# Context API - Behaviors

## With regard to the React Context API, what does a “provider” do?

- responsible for both displaying the local state of the snackbars (we call them alerts), and for exposing an API for globally managing them.

## With regard to the React Context API, how would we implement a “consumer” role?

- It turns out that our custom hook from before is nothing more than a small wrapper around the useContext internal React hook, which consumes our new context.


## Specifically with Context, how are we “wrapping” components to achieve our goals?

- Using the context object and the provider component, we will wrap all our components with which we want to share the data. But rather than rendering them from Context.js, we will use their parent component to wrap all of its child components who need the data.

- In context.js, we can access those child components from App.js through props, so here we will simply render {props.children} in the Provider Component with a required prop as value, in which we need to pass the data which we want to share i.e. the blogs state in our case. Note that, we can share the context (data) only if we are passing it through this value prop.

- last step is to consume the context value in the required components using the useContext hook by:
  
1.	Go to the required Component and import the useContext hook from React and BlogContext from context.js 

2.	We use the context object to get the context value (i.e. data) from the Provider component using the useContext method of React. This useContext method accepts the context object as its argument and returns the current context value.


## CONCLUSION :

- Using the createContext() method of React, we create the context object.

- Pull out the Provider from the context object.

- Wrap all the required components in the parent component with the Provider.

- Lastly, consume the context with the useContext() hook and use it as you want.


