# # Reading: useEffect() Hook

If you’re familiar with React class lifecycle methods, you can think of ***useEffectHook***  as ***componentDidMount, componentDidUpdate, and componentWillUnmount combined***.

1.	What purpose does useEffect serve in a function component compared to its counterpart(s) in class components?
The Effect Hook lets you perform side effects in function components.

all examples of side effects:

a.	Data fetching

b.	setting up a subscription

c.	manually changing the DOM


2.	What does useEffect do?
 By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.

3.	Why is useEffect called inside a component?

Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect. We don’t need a special API to read it — it’s already in the function scope. Hooks embrace JavaScript closures and avoid introducing React-specific APIs where JavaScript already provides a solution.

4.	Does useEffect run after every render? 

Yes! By default, it runs both after the first render and after every update. 

5.	Explain the importance of properly implementing effects with Cleanup

Some effects require cleanup. For example, we might want to set up a subscription to some external data source. In that case, it is important to clean up so that we don’t introduce a memory leak!

6.	Why did we return a function from our effect? 

This is the optional cleanup mechanism for effects. Every effect may return a function that cleans up after it. This lets us keep the logic for adding and removing subscriptions close to each other. They’re part of the same effect!

7.	When exactly does React clean up an effect? 

React performs the cleanup when the component unmounts. However, as we learned earlier, effects run for every render and not just once. This is why React also cleans up effects from the previous render before running the effects next time.

