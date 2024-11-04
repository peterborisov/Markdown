### Patterns - https://javascriptpatterns.vercel.app/patterns/react-patterns/higher-order-component

### Q&A

**1. React vs. Angular**
||Angular|React|
|:---|:---|:---|
||Framework| Library|
|Author|Google| Facebook|
|Architecture|Complete MVC(MVVM)|View layer of MVC|
|DOM|Real DOM|Virtual DOM|
|Data-Binding|Bi-directional|One way|
|Rendering|Client-Side|Server-Side|
|Performance|Slow|Faster due to Virtual DOM|

- One way data binding(user click, handle event, update state). Child components are not able to update parent data. Angular is two ways(watcher update state and view at the same time).

**2. Lifecycle methods of component**

- Initialization: the component is constructed with the given Props and default state.
- Mounting: rendering the JSX returned by the render method itself.
- Updating:the state of a component is updated.
- Unmounting:the component is removed from the page.

**3. CORS in React**

- allows you to make requests to the server deployed at a different domain.

**4. Axios**

- send asynchronous HTTP requests to REST endpoints. This library is very useful to perform CRUD operations.

**5. What are controlled components and uncontrolled components?**

- Controlled: state and behaviors are controlled by Parent components via props
- Uncontrolled: control of their own state and manage the behaviors on themselves

**6. What are Pure components?**

- only re-render when their props or state change.

**7. Pass state data**

- Parent to Child (via props)
- Child to Parent (via callback functions)
- Sibling to Sibling
- Using Context API
- Using State Management Libraries

**8. How to Handle Errors in React Applications?**

- Try/Catch in Event Handlers
- Error State in Hooks
- PropTypes
- Strict Mode

**9. How to optimize the performance of React app.**

- Code Splitting: Split your code into smaller chunks using tools like Webpack or React.lazy() to load only what is necessary for each page or component.
- Bundle Size Reduction
- Lazy Loading: Load components and resources only when they are needed, improving initial load time and reducing data transferred
- Memoization: Use React’s `memo` or `PureComponent` to memoize components and prevent unnecessary re-renders when props or state haven’t changed.
- Server-Side Rendering (SSR): Implement SSR to pre-render React components on the server, reducing initial load time and improving SEO.

10. How to Secure Your React.js Application

- HTTPS
- Avoid Storing Sensitive Data
- Implement Authentication

#### 11. Differentiate between Real DOM and Virtual DOM.

| Real DOM                                 | Virtual DOM                            |
| :--------------------------------------- | :------------------------------------- |
| 1. It updates slow.                      | 1. It updates faster.                  |
| 2. Can directly update HTML.             | 2. Can’t directly update HTML.         |
| 3. Creates a new DOM if element updates. | 3. Updates the JSX if element updates. |
| 4. DOM manipulation is very expensive.   | 4. DOM manipulation is very easy.      |
| 5. Too much of memory wastage.           | 5. No memory wastage.                  |

#### 12. List some of the major advantages of React.

- Virtual DOM improve efficiency
- Gentle learning curve
- SEO friendly
- Increases performance
- It can be conveniently used on the client as well as server side
- Because of JSX, code’s readability increases

#### 13. What are the limitations of React?

- React is just a library, not a full-blown framework

#### 8. Why can’t browsers read JSX?

- Browsers can only read JavaScript objects but JSX in not a regular JavaScript object. Thus to enable a browser to read JSX, first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel and then pass it to the browser.

#### 14. How different is React’s ES6 syntax when compared to ES5?

|                        | ES5 | ES6 |
| :--------------------- | :-- | :-- |
| require vs import      |
| export vs exports      |
| component and function |
| props                  |
| state                  |

#### 15. How is React different from Angular?

|              | React                  | Angular               |
| :----------- | :--------------------- | :-------------------- |
| ARCHITECTURE | Only the View of MVC   | Complete MVC          |
| RENDERING    | Server-side rendering  | Client-side rendering |
| DOM          | Uses virtual DOM       | Uses real DOM         |
| DATA BINDING | One-way data binding   | Two-way data binding  |
| DEBUGGING    | Compile time debugging | Runtime debugging     |
| AUTHOR       | Facebook               | Google                |

#### 16. What is the purpose of render() in React.

- Each React component must have a render() mandatorily. It returns a single React element which is the representation of the native DOM component. This function must be kept pure i.e., it must return the same result each time it is invoked.

#### 17. Explain the lifecycle methods of React components in detail

- **componentWillMount()**– Executed just before rendering takes place both on the client as well as server-side.
- **componentDidMount()** – Executed on the client side only after the first render.
- **componentWillReceiveProps()** – Invoked as soon as the props are received from the parent class and before another render is called.
- **shouldComponentUpdate()** – Returns true or false. If you want your component to update, return true else return false. By default, it returns false.
- **componentWillUpdate()** – Called just before rendering takes place in the DOM.
- **componentDidUpdate()** – Called immediately after rendering takes place.
- **componentWillUnmount()** – Called after the component is unmounted from the DOM. It is used to clear up the memory spaces.

#### 18. What is an event in React?

Similar to handling events in DOM elements.

- Events are named using camel case instead of just using the lowercase.
- Events are passed as functions instead of strings.

#### 19. What are synthetic events in React?

- Synthetic events are the objects which act as a cross-browser wrapper around the browser’s native event. They combine the behavior of different browsers into one API. This is done to make sure that the events show consistent properties across different browsers.

#### 20. What do you understand by refs in React?

- It is an attribute which makes it possible to store a reference. It provides a way to access React DOM nodes or React elements. It is used when we want to change the value of a child component, without making the use of props.

#### 21. List some of the cases when you should use Refs.

- When you need to manage focus, select text or media playback
- To trigger imperative animations
- Integrate with third-party DOM libraries

#### 22. How do you modularize code in React?

- By using the export and import properties.

#### 23. What do you know about controlled and uncontrolled components?

- Controlled component - the value of the input element is controlled by React. Any changes made to the input element will be reflected in the code as well. When a user enters data inside the input element of a controlled component, onChange function gets triggered and inside the code we check whether the value entered is valid or invalid. If the value is valid, we change the state and re-render the input element with new value.
- Uncontrolled component In an uncontrolled component, the value of the input element is handled by the DOM itself.

| Controlled Components                                                                      | Uncontrolled Components                      |
| :----------------------------------------------------------------------------------------- | :------------------------------------------- |
| 1. They do not maintain their own state                                                    | 1. They maintain their own state             |
| 2. Data is controlled by the parent component                                              | 2. Data is controlled by the DOM             |
| 3. They take in the current values through props and then notify the changes via callbacks | 3. Refs are used to get their current values |

#### 24. What is the significance of keys in React?

- Keys are used for identifying unique Virtual DOM Elements

#### 25. What is the use of render() in React?

- returns the HTML, which is to be displayed in the component.
- If you need to render more than one element, all of the elements must be inside one parent tag.

#### 26. How do you style React components?

- Inline Styling(style={{ color: "Yellow" }})
- JavaScript Object( myStyle = {color: "red", fontSize: "28px"})
- CSS Stylesheet(import './RandomComponent.css';)
- CSS Modules(.module.css)

#### 27. How to prevent re-renders in React?

- Re-rendering of a component and it’s child components occur when props or state of the component has been changed. Use the shouldComponentUpdate( ) method.

#### 28. Explain React Hooks.

- Hooks are functions that let us “hook into” React state and lifecycle features from a functional component.
  React Hooks cannot be used in class components. They let us write components without class.

#### 29. Name a few techniques to optimize React app performance.

- useMemo( ) -It is a React hook that is used for caching CPU-Expensive functions.
- React.PureComponent
- Maintaining State Colocation
- Lazy Loading

#### 30. What is prop drilling in React?

- Pass data levels down to nested components. The disadvantage of using prop drilling is that the components that should otherwise be not aware of the data have access to the data.

#### 31. What is Context in React?

- Context provide a way to pass data through the component three without passing props down manually at every level

## React Router

#### 1. What is React Router?

- React Router is a powerful routing library built on top of React.

#### 2. How is React routing different from conventional routing?

| React Routing                                       | Conventional routing                            |
| :-------------------------------------------------- | :---------------------------------------------- |
| Single HTML page                                    | Each view is a new HTML file                    |
| The user navigates multiple views in the same file  | The user navigates multiple files for each view |
| The page does not refresh since it is a single file | The page refreshes every time user navigates    |
| Improved performance                                | Slower performance                              |
