### Cheat sheet - https://zerotomastery.io/cheatsheets/react-cheat-sheet/

### Patterns - https://javascriptpatterns.vercel.app/patterns/react-patterns/higher-order-component

### Q&A

**1. Building blocks of React**

- **Components**: Reusable blocks of code that return HTML.
- **JSX**: It stands for JavaScript and XML and allows you to write HTML in React.
- **Props and State**: props are like function parameters and State is similar to variables.
- **Context**: This allows data to be passed through components as props in a hierarchy.
- **Virtual DOM**: It is a lightweight copy of the actual DOM which makes DOM manipulation easier.

**2. Props and State in React with differences**

- **Props** pass data from one component to another.
- **State** is local data storage

**3. What is virtual DOM in React**

- Lightweight copy of the actual DOM. Manipulating Virtual DOM is more faster.

**4. React Components**

- **Functional Components**: Functional components are simply javascript functions.
- **Class Components**:

**5. React vs. Angular**

- React is library. Angular is framework.
- React is view from MVC. Angular is MVVM.
- React is one way data binding(user click, handle event, update state). Child components are not able to update the data that is coming from the parent component. Angular is two ways(watcher update state and view at the same time).
- React VDOM. Angular DOM.

**6. React state**

- Object to keep some information about component.

**7. React Props.**

- objects which can be used inside a component

**8. Higher-order component**

- Takes the original component and returns the enhanced component. Helps to get rid of copying the same logic in every component.

**9. Functional vs. Class component**

- Function component:
  - Plain JavaScript pure function
  - No render method
  - Stateless
  - No lifecycle methods
  - No Constructors

**10. Lifecycle methods of component**

- Initialization: the component is constructed with the given Props and default state.
- Mounting: rendering the JSX returned by the render method itself.
- Updating:the state of a component is updated.
- Unmounting:the component is removed from the page.

11. Ref in React

- function provided by React to access the DOM element and the React element that you might have created on your own.

**12. Hooks**

- Reusable functions that allows you to use state and other React features without writing a class.
  - **useState**: store component values.
  - **useEffect**: Create side effect(action which is not related to current component).
  - **useLayoutEffect** - run immediately after DOM changes
  - **useRef**: like useState but doesn't rerender component if ref data is updated.
  - **useMemo**: memoize the result of a function.
  - **useCallback**: memoize callbacks. Prevents functions recreated between re-renders.
  - **useContext**: Allows you to consume context(Context provides a way to pass data through the component tree without having props drilling.) in functional components.
  - **useReducer**: Alternative to useState for managing more complex state logic. It accepts a reducer function and an initial state, returning the current state and a dispatch function to trigger state updates.

```
  reducer(state, action)
```

- custom hooks: normal JS functions start with "use". It helps us to write a logic once and use it anywhere in the code. Extract reusable logic.

**13. React Fragments**

- wrap more than one root elements

**14. How to optimize a React code?**

- meaningful component names
- Break down components
- destructuring
- prop-types
- functional components
- Avoid using inline styles
- arrow functions
- spread operator

**15. CORS in React**

- allows you to make requests to the server deployed at a different domain.

**16. Axios**

- send asynchronous HTTP requests to REST endpoints. This library is very useful to perform CRUD operations.

**17. How the Virtual DOM works**

- React crate copy of the real DOM.
- On component render, React creates Virtual DOM representation in memory.
- On state or props change, React creates a new Virtual DOM representation.
- Compares the new Virtual DOM with the previous one.
- Updates the real DOM

**18. How VDOM improves performance**

- grouping multiple updates together before applying them to the real DOM
- It only updates the specific components or elements that have changed

**19. What are controlled components and uncontrolled components?**

- Controlled: state and behaviors are controlled by Parent components via props
- Uncontrolled: control of their own state and manage the behaviors on themselves

**20. What are Pure components?**

- only re-render when their props or state change.

**21. Pass state data**

- Parent to Child (via props)
- Child to Parent (via callback functions)
- Sibling to Sibling
- Using Context API
- Using State Management Libraries

**22. What is the difference between stateful and stateless React?**

- Stateful(Class) can modify state
- Stateless(Functional) components print out what is given to them via props, or they always render the same thing.

**23. What is state in React?**

- Object that is used to contain data or information about the component.
- When state change, component re-render.

**24. What are props in React?**

- Mechanism for passing data from a parent to child.

**25. How to Handle Errors in React Applications?**

- Try/Catch in Event Handlers
- Error State in Hooks
- PropTypes
- Strict Mode

**26. How to optimize the performance of React app.**

- Code Splitting: Split your code into smaller chunks using tools like Webpack or React.lazy() to load only what is necessary for each page or component.
- Bundle Size Reduction
- Lazy Loading: Load components and resources only when they are needed, improving initial load time and reducing data transferred
- Memoization: Use React’s `memo` or `PureComponent` to memoize components and prevent unnecessary re-renders when props or state haven’t changed.
- Server-Side Rendering (SSR): Implement SSR to pre-render React components on the server, reducing initial load time and improving SEO.

27. How to Secure Your React.js Application

- HTTPS
- Avoid Storing Sensitive Data
- Implement Authentication

### React concept

- One way data flow
- Declarative vs Imperative

### Types of React Components

**- Stateless/Presentational/Dumb/Pure Components** - always produce the same output for the same input props and do not have any side effects. Primarily used for rendering UI elements and do not contain any logic or state management.

- **Stateful/Container/Smart/Impure Components** - may produce different output for the same input props or have side effects. Impure components are typically used for managing state, handling complex logic, making API calls, or interacting with the DOM.
- **Higher Order Components (HOCs)** - functions that take a component as input and return a new component with additional props or behavior. HOCs are used for reusing component logic, such as handling authentication, handling data fetching, or providing common functionality to multiple components.
- **Controlled Component** - whenever a component is connected to a state, so that we can manage data, then its a controlled component. A controlled component allows Two Way Binding , where we both use and update its data programmatically.

### Hooks

https://react-v8.holt.courses/lessons/hooks-in-depth/useref
https://tanstack.com

- useRef() - refer react element to the DOM element
- useReducer()
- useMemo() - memoize result of expensive calculations

```
const value = useMemo(() => {someExpensiveOperation(count)}, [count])
```

- useCallback() - memoize callback fn similar to useMemo. Save a function at one place in memory and not recreate it with every execution.

```
const memoizedCAllback = useCallback(() => {myFn()}, [])
```

### TailwindCSS

- TailwindCSS for css classes, grid/flex, etc.
- https://flowbite-react.com for UI components

### Lint, Prettier, Husky

https://medium.com/yavar/setting-up-a-eslint-prettier-husky-and-lint-staged-integration-with-typescript-in-next-js-13-14-68044dfae920

### Advanced React performance

- Code splitting
  https://bundlephobia.com
- SSR

### Testing

https://nextjs.org/docs/app/building-your-application/testing/jest


https://github.com/sudheerj/reactjs-interview-questions#what-is-react

https://www.simplilearn.com/tutorials/reactjs-tutorial/reactjs-interview-questions

https://www.edureka.co/blog/interview-questions/react-interview-questions/

## General React
#### 1. Differentiate between Real DOM and Virtual DOM.
|Real DOM|Virtual DOM|
|:---|:---|
|1. It updates slow.|1. It updates faster.|
|2. Can directly update HTML.|2. Can’t directly update HTML.|
|3. Creates a new DOM if element updates.|3. Updates the JSX if element updates.|
|4. DOM manipulation is very expensive.|4. DOM manipulation is very easy.|
|5. Too much of memory wastage.|5. No memory wastage.|

#### 2. What is React?
- React is a front-end JavaScript library developed by Facebook in 2011.
- It follows the component based approach which helps in building reusable UI components.
- It is used for developing complex and interactive web and mobile UI. 

#### 3. What are the features of React? 
- It uses the virtual DOM instead of the real DOM.
- It uses server-side rendering.
- It follows uni-directional data flow or data binding.

#### 4. List some of the major advantages of React.
- Virtual DOM improve efficiency
- Gentle learning curve
- SEO friendly
- Increases performance
- It can be conveniently used on the client as well as server side
- Because of JSX, code’s readability increases

#### 5. What are the limitations of React?
- React is just a library, not a full-blown framework
- Its library is very large and takes time to understand

#### 6. What is JSX?
- JSX is a shorthand for JavaScript XML.

#### 7. What do you understand by Virtual DOM? Explain its working.
- VDOM is just the copy of the real DOM. It is a node tree that lists the elements, their attributes and content as Objects and their properties. React’s render function creates a node tree out of the React components. It then updates this tree in response to the mutations in the data model which is caused by various actions done by the user or by the system.
- Virtual DOM works in three simple steps.
    1. If data changes, the entire UI is re-rendered in Virtual DOM representation.
    2. The difference is calculated.
    3. The real DOM will be updated with only the things that have actually changed.

#### 8. Why can’t browsers read JSX?
- Browsers can only read JavaScript objects but JSX in not a regular JavaScript object. Thus to enable a browser to read JSX, first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel and then pass it to the browser.

#### 9. How different is React’s ES6 syntax when compared to ES5?
||ES5|ES6|
|:---|:---|:---|
|require vs import
|export vs exports
|component and function
|props
|state

#### 10. How is React different from Angular?
1. ARCHITECTURE	| Only the View of MVC | Complete MVC
2. RENDERING | Server-side rendering	| Client-side rendering
3. DOM | Uses virtual DOM | Uses real DOM
4. DATA BINDING | One-way data binding | Two-way data binding
5. DEBUGGING | Compile time debugging | Runtime debugging
6. AUTHOR | Facebook | Google

## React Components
> Components are the building blocks of a React application’s UI. These components split up the entire UI into small independent and reusable pieces. Then it renders each of these components independent of each other without affecting the rest of the UI.

#### 1. What is the purpose of render() in React.
- Each React component must have a render() mandatorily. It returns a single React element which is the representation of the native DOM component. This function must be kept pure i.e., it must return the same result each time it is invoked.

#### 2. What is Props?
- the way to pass data between components.
- one way from parent to child.
- props data is read-only, which means that data coming from the parent should not be changed by child components.

#### 3. What is a state in React and how is it used?
- The state object is where you store property values that belongs to the component.
- When the state object changes, the component re-renders.

#### 4. Differentiate between states and props.
||State|Props|
|:---|:---|:---|
Use|Holds information about the components|Allows to pass data from one component to other components as an argument
Mutability|Is mutable|Are immutable
Read-Only| Can be changed| Are read-only
Child components| Child components cannot access |Child component can access 

#### 5. How can you update the state of a component?
- using this.setState().

#### 6. Differentiate between stateful and stateless components.
||Stateful(Class) Component|	Stateless(Functional) Component|
|:---|:---|:---|
State| Can hold or manage state| Cannot hold or manage state
Simplicity|Complex as compared to the stateless component|Simple and easy to understand
Lifecycle methods|Can work with all lifecycle methods|Does not work with any lifecycle method
Reusability|Can be reused|Cannot be reused

#### 7. What are the different phases of React component’s lifecycle?
- There are three different phases:
1. **Initial Rendering Phase(Mounting)**:  Component is about to start its life journey and make its way to the DOM.
2. **Updating Phase(Updating)**: It can potentially update and re-render only when a prop or state change occurs.
3. **Unmounting Phase(Unmounting)**: The component is destroyed and removed from the DOM.

#### 8. What are Higher Order Components(HOC)
- Acts as a container for other components. This helps to keep components simple and enables re-usability. They are generally used when multiple components have to use a common logic. Function that takes in a component and returns a new component

#### 9. What are Pure Components?
- Pure components are the simplest and fastest components which can be written. They can replace any component which only has a render(). These components enhance the simplicity of the code and performance of the application.

## React 
#### 1.  Explain the lifecycle methods of React components in detail
 - **componentWillMount()**– Executed just before rendering takes place both on the client as well as server-side.
- **componentDidMount()** – Executed on the client side only after the first render.
- **componentWillReceiveProps()** – Invoked as soon as the props are received from the parent class and before another render is called.
- **shouldComponentUpdate()** – Returns true or false. If you want your component to update, return true else return false. By default, it returns false.
- **componentWillUpdate()** – Called just before rendering takes place in the DOM.
- **componentDidUpdate()** – Called immediately after rendering takes place.
- **componentWillUnmount()** – Called after the component is unmounted from the DOM. It is used to clear up the memory spaces.

#### 2. What is an event in React?
Similar to handling events in DOM elements.
- Events are named using camel case instead of just using the lowercase.
- Events are passed as functions instead of strings.

#### 3. What are synthetic events in React?
- Synthetic events are the objects which act as a cross-browser wrapper around the browser’s native event. They combine the behavior of different browsers into one API. This is done to make sure that the events show consistent properties across different browsers.

#### 4. What do you understand by refs in React?
- It is an attribute which makes it possible to store a reference. It provides a way to access React DOM nodes or React elements. It is used when we want to change the value of a child component, without making the use of props.

#### 5. List some of the cases when you should use Refs.

- When you need to manage focus, select text or media playback
- To trigger imperative animations
- Integrate with third-party DOM libraries

#### 6. How do you modularize code in React?
- By using the export and import properties.

#### 7. What do you know about controlled and uncontrolled components?
- Controlled component - the value of the input element is controlled by React. Any changes made to the input element will be reflected in the code as well. When a user enters data inside the input element of a controlled component, onChange function gets triggered and inside the code we check whether the value entered is valid or invalid. If the value is valid, we change the state and re-render the input element with new value.
- Uncontrolled component In an uncontrolled component, the value of the input element is handled by the DOM itself.

|Controlled Components|	Uncontrolled Components|
|:---|:---|
|1. They do not maintain their own state	|1. They maintain their own state
|2. Data is controlled by the parent component|	2. Data is controlled by the DOM
|3. They take in the current values through props and then notify the changes via callbacks	|3. Refs are used to get their current values

#### 8. What is the significance of keys in React?
- Keys are used for identifying unique Virtual DOM Elements

#### 9. What is the use of render() in React?
- returns the HTML, which is to be displayed in the component.
- If you need to render more than one element, all of the elements must be inside one parent tag.

#### 10. How do you style React components?
- Inline Styling(style={{ color: "Yellow" }})
- JavaScript Object( myStyle = {color: "red", fontSize: "28px"})
- CSS Stylesheet(import './RandomComponent.css';)
- CSS Modules(.module.css)

#### 11. How to prevent re-renders in React?
- Re-rendering of a component and it’s child components occur when props or state of the component has been changed. Use the shouldComponentUpdate( ) method.

#### 12. Explain React Hooks. 
- Hooks are functions that let us “hook into” React state and lifecycle features from a functional component.
React Hooks cannot be used in class components. They let us write components without class.

#### 13. Name a few techniques to optimize React app performance.
- useMemo( ) -It is a React hook that is used for caching CPU-Expensive functions.
- React.PureComponent
- Maintaining State Colocation
- Lazy Loading 

#### 14. What is prop drilling in React? 
- Pass data levels down to nested components. The disadvantage of using prop drilling is that the components that should otherwise be not aware of the data have access to the data.

#### 15. What is Context in React?
- Context provide a way to pass data through the component three without passing props down manually at every level

## React Router
#### 1. What is React Router?
- React Router is a powerful routing library built on top of React.
#### 2. How is React routing different from conventional routing?
|React Routing|Conventional routing
|:---|:---|
|Single HTML page|Each view is a new HTML file
|The user navigates multiple views in the same file|The user navigates multiple files for each view
The page does not refresh since it is a single file|The page refreshes every time user navigates
Improved performance|Slower performance


# React 
Open-source, component-based, front-end library responsible only for the application’s view layer. In Model View Controller (MVC) architecture, the view layer is responsible for how the app looks and feels.

## Why React?
- **Easy creation of dynamic applications:** React makes it easier to create dynamic web applications because it requires less coding and offers more functionality.<br>
- **Improved performance:** React uses Virtual DOM, thereby creating web applications faster. Virtual DOM compares the components’ previous states and updates only the items in the Real DOM that were changed.<br>
- **Reusable components**
- **Unidirectional data flow:** React follows a unidirectional data flow. This means that when designing a React app, developers often nest child components within parent components.<br>
- **Small learning curve:** React is easy to learn, as it mostly combines basic HTML and JavaScript concepts with some beneficial additions.<br>
- **It can be used for the development of both web and mobile apps**
- **Dedicated tools for easy debugging**

## 10 basic concepts of React
 1. **Virtual DOM(VDOM)** 
>- lightweight representation of the 'real' DOM in the memory. When the state of an object changes, VDOM changes only that object in the real DOM instead of updating all of the objects. Synced with the real DOM by a library such as ReactDOM. <br>
 2. **JSX**
> - JavaScript Syntax Extension. By using JSX, we can write HTML structures in the same file that contains JavaScript code.<br>
3. **Embedding expressions in JSX**
> ```
> const user = “Tom Cruise”
> const jsxElement = <h1> Hello, {user} </h1>
> ```
 4. **React Elements** 
> - Elements are the building blocks for components.<br>
 5. **Rendering Elements**
> - React apps usually have a single root DOM node in the HTML file, which is div id="root" and react DOM manages everything inside it. In order to render a react element in the root DOM node, both of them have to passed into ReactDOM.render().<br>
6.  **Components**
> - Components are functions that take inputs as props and return the elements for UI.\
4 ways to create react component:<br>
> createClass<br>
> ES class<br>
> Function<br>
> Arrow function
7. **Class Components**
>```
>class Greeting extends React.Component {
>    render () {
>         <h1>Hello, {this.props.name}</h1>
>        }
>}
>```
8. **Component rendering**
> - Rendering a component is the same as rendering an element.<br>
9. **Component Lifecycle** 
> -  mounting - rending component.<br>
constructor() => render() => componentDidMount()
> -  updating - change props or state<br>
> render() => componentDidUpdate()
> -  unmounting - remove component<br> componentWillUnmount
10. **Other APIs and Properties** 
>- setState() forceUpdate()

## Components, State, and Props
**Components**<br>
> A component is essentially a piece of the user interface. React splits the UI into independent, reusable parts that can be processed separately.
> - **Stateless Functional** - These components have no state of their own and only contain a render method, so they are also called stateless components. They may derive data from other components as props (properties).
> - **Statefull Class** - These components can hold and manage their state and have a separate render method for returning JSX on the screen. They are also called stateful components, as they can have a state.

**State** <br>
> The state is a built-in React object that is used to contain data or information about the component. A component’s state can change over time; whenever it changes, the component re-renders.

 **Props**<br>
>It provides a way to pass data from one component to other components in the same way as arguments are passed in a function. Props are read-only, the data coming from a parent component can't be changed by the child component. 
> - Define an attribute and its value - 'Child attr1={value} attr2={value}'
> - Pass it to child component or components by using props - Passing props is simple, and we can add props like we pass an argument to a function.
> - Render the props data - Child text={"Child 1"}

## State vs. Props

|             | State       | Props     |
| :---        |    :----:   |          :---: |
| Use case    | State is used to store the data of the components that have to be rendered to the view | Props are used to pass data and event handlers to the children components  | Props are used to pass data and event handlers to the children components
| Mutability  | State holds the data and can change over time        | Props are immutable—once set, props can't be changed     |
| Component   | State can only be used in class components        | Props can be used in both functional and class components      |
| Updation    | Event handlers generally update state        | The parent component sets props for the children components      |

## React Components Lifecycle
Each component in React has a life-cycle that you can monitor and change during its three main phases.<br>
**Mounting**
> - component is mounted on the DOM and then rendered on the webpage.<br>
> 1. **componentWillMount()** - This function is called right before we mount the component on the DOM. So after this method executes, the component gets mounted on the DOM.
> 2. **render()** - This function mounts the component on the browser.
> 3. **componentDidMount()** - We invoke this function right after the component is mounted on the DOM. Generally, in React applications, we do the API calls within this method.

**Updating**
> - We call the methods in this phase whenever State or Props in a component get updated. 
> 1. **componentWillReceiveProps()** - We call This function before a component gets its props reassigned. 
> 2. **setState()** - This function can be called explicitly at any moment. This function is used to update the state of a component.
> 3. **shouldComponentUpdate()** - This function is called before rendering a component and tells React whether it should update the component on receiving new props or state. 
> 4. **componentWillUpdate()** - This function is called once before the render() function is executed after the update of State or Props.
> 5. **render()** - The component gets rendered when this function is called.
> 6. **componentDidUpdate()** - This function is called once after the render() function is executed after the update of State or Props.

**Unmounting**
> - This is the last phase of the life-cycle of the component where the component is unmounted from the DOM. 
> 1. **componentWillUnmount()** - This function is called once before we remove the component from the page and this marks the end of the life-cycle.