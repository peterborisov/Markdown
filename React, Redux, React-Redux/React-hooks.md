React hook makes use of hidden state of a component, it's stored inside a fiber, a fiber is an entity that corresponds to component instance (in a broader sense, because functional components don't create instances as class components).

## Basic hooks
- **useState**
- Allows functional components to have a dedicated state of their own
- Type of state - Number, String, Boolean
```
const [count, setCount] = useState(0);
const handleIncrement = () => {
    setCount(count + 1);
};
<button onClick={handleIncrement}>
    Click me
</button>
```
- **useEffect**<br/>
- Allows functional components to manipulate DOM elements before each render.
- The function **useEffect** takes a callback function as its first parameter. That callback function will be executed every time re-render component. If you don’t want it to be executed after each re-render, then you will have to add a second parameter(empty array).
```
useEffect(()=>{
  console.log(123);
},[]);
```
- Only when the value someParam renders or changes, the callback runs, and the side effect will be performed.
```
useEffect(()=>{
  console.log('Only run on someParam change')
},[someParam]);
```

- **useContext**<br/>
Context provides way to pass data throught conponent tree without having pass props down manually at every level.
 ```
 const someContextName = useContext(MyContextComp) 
 ```

## Additional hooks
- **useReducer**
- Type of state - Object or Array
- The useReducer hook takes three arguments including reducer, initial state, and the function to load the initial state lazily.
```
const [state, dispatch] = useReducer(reducer, initialArgs, init);
```
```
import React, { useReducer } from 'react'

const initialState = {
	firstCounter: 0,
	secondCounter: 10
}
const reducer = (state, action) => {
	switch (action.type) {
		case 'increment':
			return { ...state, firstCounter: state.firstCounter + action.value }
		case 'increment2':
			return { ...state, secondCounter: state.secondCounter + action.value }
		case 'reset':
			return initialState
		default:
			return state
	}
}

const CounterTwo = () => {
	const [count, dispatch] = useReducer(reducer, initialState)

	return (
		<>
			<div>Count = {count.firstCounter}</div>
			<button onClick={() => dispatch({ type: 'increment', value: 1 })}>
				Increment
			</button>
			<button onClick={() => dispatch({ type: 'increment', value: 5 })}>
				Increment 5
			</button>

			<button onClick={() => dispatch({ type: 'reset' })}>Reset</button>

			<div>Secound Counter = {count.secondCounter}</div>
				<button onClick={() => dispatch({ type: 'increment2', value: 1 })}>
					Increment
				</button>
		</>
	)
}
export default CounterTwo;

https://www.youtube.com/watch?v=IHJ-TO_1nME
https://www.youtube.com/watch?v=uX7lxFrWUbA
https://github.com/gopinav/React-Tutorials/blob/master/React%20Hooks/reducer-hook/src/components/CounterTwo.js
```

- **useCallback**
- The useCallback hook is used when you have a component in which the child is rerendering again and again without need.
- Hook that will return a memoized version of the callback function that only changes if one of the dependencies has changed.
- It’s very useful when a component is passing a callback to its child component to prevent the rendering of the child component.

```
const memoizedCallback = useCallback( 
  () => {doSomething(a, b);},
  [a, b],
);
```

- **useMemo**
- Memorized the value that only changes if one of the dependencies has changed.
- It recalculated the value only when one of its dependencies change. 
- It is useful to avoid expensive calculations on every render when the returned value is not going to change.
```
const memoizedValue = useMemo(functionThatReturnsValue, arrayDepencies)
```
```
const isEven = useMemo(() => {
  while(i < 2000000) i++
  return counter % 2 === 0
},[counter])
```
- **useRef**
- Returns a mutable ref object whose .current property is initialized to the passed argument (initialValue).
- A common use case is to access dom/ child component properties.

- **useImperativeHandle**
- **useLayoutEffect**
- **useDebugValue**

## Custom hooks
- JS function whose name starts with 'use'.
- Can call other hooks if required.
- Share logic between components.
