# Redux - Asynchronous Actions

## Async Logic and Data Fetching

- how do middleware and async logic affect the overall data flow of a Redux app?

Just like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.

Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.

Earlier, we saw a diagram that represents the normal synchronous Redux data flow. When we add async logic to a Redux app, we add an extra step where middleware can run logic like AJAX requests, then dispatch actions.

- Why Do I Need This?
- 
With a plain basic Redux store, you can only do simple synchronous updates by dispatching an action. Middleware extends the store's abilities, and lets you write async logic that interacts with the store.

Thunks are the recommended middleware for basic Redux side effects logic, including complex synchronous logic that needs access to the store, and simple async logic like AJAX requests.

## Redux Thunk
Thunk middleware for Redux. It allows writing functions with logic inside that can interact with a Redux store's dispatch and getState methods.

### Installation and Setup

- Redux Toolkit

If you're using our official Redux Toolkit package as recommended, there's nothing to install - RTK's configureStore API already adds the thunk middleware by default:
```js
import { configureStore } from '@reduxjs/toolkit'

import todosReducer from './features/todos/todosSlice'
import filtersReducer from './features/filters/filtersSlice'

const store = configureStore({
  reducer: {
    todos: todosReducer,
    filters: filtersReducer
  }
})

// The thunk middleware was automatically added
```

- Manual Setup

If you're using the basic Redux createStore API and need to set this up manually, first add the redux-thunk package:

npm install redux-thunk

yarn add redux-thunk
The thunk middleware is the default export.

More Details: Importing the thunk middleware
Then, to enable Redux Thunk, use applyMiddleware():
```js
import { createStore, applyMiddleware } from 'redux'
import thunk from 'redux-thunk'
import rootReducer from './reducers/index'

const store = createStore(rootReducer, applyMiddleware(thunk))
```
- Injecting a Custom Argument

Since 2.1.0, Redux Thunk supports injecting a custom argument into the thunk middleware. This is typically useful for cases like using an API service layer that could be swapped out for a mock service in tests.

For Redux Toolkit, the getDefaultMiddleware callback inside of configureStore lets you pass in a custom extraArgument:

```js 
import { configureStore } from '@reduxjs/toolkit'
import rootReducer from './reducer'
import { myCustomApiService } from './api'

const store = configureStore({
  reducer: rootReducer,
  middleware: getDefaultMiddleware =>
    getDefaultMiddleware({
      thunk: {
        extraArgument: myCustomApiService
      }
    })
})

// later
function fetchUser(id) {
  // The `extraArgument` is the third arg for thunk functions
  return (dispatch, getState, api) => {
    // you can use api here
  }
}
```
If you need to pass in multiple values, combine them into a single object:
```js
const store = configureStore({
  reducer: rootReducer,
  middleware: getDefaultMiddleware =>
    getDefaultMiddleware({
      thunk: {
        extraArgument: {
          api: myCustomApiService,
          otherValue: 42
        }
      }
    })
})

// later
function fetchUser(id) {
  return (dispatch, getState, { api, otherValue }) => {
    // you can use api and something else here
  }
}```

