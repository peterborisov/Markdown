React hook makes use of hidden state of a component, it's stored inside a fiber, a fiber is an entity that corresponds to component instance (in a broader sense, because functional components don't create instances as class components).

## Basic hooks
- **useState**
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
The function **useEffect** takes a callback function as its first parameter. That callback function will be executed every time re-render component. If you don’t want it to be executed after each re-render, then you will have to add a second parameter(empty array).
```
useEffect(()=>{
  console.log(123);
},[]);
```
Only when the value someParam renders or changes, the callback runs, and the side effect will be performed.
```
useEffect(()=>{
  console.log('Only run on someParam change')
},[someParam]);
```

- **useContext**<br/>
 Make use of Context and acts like a consumer and not Provider. 
 ```
 const someContexName = useContext(MyContexComp) 
 ```

## Additional hooks
- **useReducer**
```
const [state, dispatch] = useReducer(reducer, initialState)
```

- **useCallback**
- **useMemo**
- **useRef**
- **useImperativeHandle**
- **useLayoutEffect**
- **useDebugValue**

## Custom hooks
