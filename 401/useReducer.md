#  Advanced State with Reducers

## useReducer hook

1.	Name an alternative to the useState Hook.

useReducer

2.	Why might the useReducer Hook be preferable to the useState Hook?

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

3.	What are two ways to set the initial state?

a.	The simplest way is to pass the initial state as a second argument:

```js
  const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}  );
```
b.	pass an init function as the third argument. The initial state will be set to init(initialArg).

```js
function Counter({initialCount}) {
  const [state, dispatch] = useReducer(reducer, initialCount, init);
}
```
It lets you extract the logic for calculating the initial state outside the reducer. This is also handy for resetting the state later in response to an action.


4.	In terms of state, what does useReducer expect to receive as a parameter?

It accepts a reducer function as its first parameter and the initial state as the second.

5.	What does useReducer return?

useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later invoke it.

6.	Explain dispatch to a non-technical recruiter.

The dispatch function accepts an object that represents the type of action we want to execute when it is called. Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state.

The action to be executed is specified in our reducer function, which in turn, is passed to the useReducer. The reducer function will then return the updated state.

The actions that will be dispatched by our components should always be represented as one object with the type and payload key, where type stands as the identifier of the dispatched action and payload is the piece of information that this action will add to the state.

The dispatch is the second value returned from the useReducer Hook and can be used in our JSX to update the state.


