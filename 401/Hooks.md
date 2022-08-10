# Reading: useState() Hook


## Introducing Hooks

1.	What was the motivation for introducing Hooks?

Hooks solve a wide variety of seemingly unconnected problems in React that we’ve encountered over five years of writing and maintaining tens of thousands of components. Whether you’re learning React, use it daily, or even prefer a different library with a similar component model, you might recognize some of these problems.

2.	What changes are important regarding implementing Hooks versus Component Classes?

There are no plans to remove classes from React. You can read more about the gradual adoption strategy for Hooks in the bottom section of this page.

Hooks don’t replace your knowledge of React concepts. Instead, Hooks provide a more direct API to the React concepts you already know: props, state, context, refs, and lifecycle. As we will show later, Hooks also offer a new powerful way to combine them.

3.	Hooks allow you to reuse stateful logic without changing  your component hierarchy.

## hooks api

1.	Name two rules imposed by React Hook usage.

Hooks are JavaScript functions, but they impose two additional rules:

•	Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.

•	Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment).

2.	How would you identify a custom Hook and why might you create one?

Custom Hooks are more of a convention than a feature. If a function’s name starts with ”use” and it calls other Hooks, we say it is a custom Hook. The useSomething naming convention is how our linter plugin is able to find bugs in the code using Hooks.

You can write custom Hooks that cover a wide range of use cases like form handling, animation, declarative subscriptions, timers, and probably many more we haven’t considered. We are excited to see what custom Hooks the React community will come up with.

## the state hook

1.	What is a Hook?

A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

2.	When would I use the useState Hook?

If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. 

3.	If you were to add React state to a function component by declaring a state variable:

1.	What does calling useState do?

It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

2.	What do we pass to useState as an argument?

The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

3.	What does useState return?

It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair. 

