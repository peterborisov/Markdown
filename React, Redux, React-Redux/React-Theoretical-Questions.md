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

- It increases the application’s performance
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

| Conditions	| State |	Props |
|:---|:---|:---|
|1. Receive initial value from parent component	|Yes|	Yes
|2. Parent component can change value |No|Yes|
|3. Set default values inside component|	Yes	|Yes|
|4. Changes inside component	|Yes|	No|
|5. Set initial value for child components	|Yes	|Yes|
|6. Changes inside child components|No|	Yes|

#### 5. How can you update the state of a component?
- using this.setState().

#### 6. Differentiate between stateful and stateless components.
|Stateful(Class) Component|	Stateless(Functional) Component|
|:---|:---|
|1. Stores info about component’s state change in memory	|1. Calculates the internal state of the components|
|2. Have authority to change state|	2. Do not have the authority to change state|
|3. Contains the knowledge of past, current and possible future changes in state	|3. Contains no knowledge of past, current and possible future state changes|
|4. Stateless components notify them about the requirement of the state change, then they send down the props to them.|	4. They receive the props from the Stateful components and treat them as callback functions.

#### 7. What are the different phases of React component’s lifecycle?
- There are three different phases:
1. **Initial Rendering Phase**:  Component is about to start its life journey and make its way to the DOM.
2. **Updating Phase**: It can potentially update and re-render only when a prop or state change occurs.
3. **Unmounting Phase**: The component is destroyed and removed from the DOM.

#### 8. What are Higher Order Components(HOC)
- Higher Order Component is a way of reusing the component logic. HOC are custom components which wrap another component within it.
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
|Controlled Components|	Uncontrolled Components|
|:---|:---|
|1. They do not maintain their own state	|1. They maintain their own state
|2. Data is controlled by the parent component|	2. Data is controlled by the DOM
|3. They take in the current values through props and then notify the changes via callbacks	|3. Refs are used to get their current values

#### 8. What is the significance of keys in React?
- Keys are used for identifying unique Virtual DOM Elements

## React Redux
#### 1. What were the major problems with MVC framework?
- DOM manipulation was very expensive
- Applications were slow and inefficient
- There was huge memory wastage

#### 2. Explain Flux.
- Flux is an architectural pattern which enforces the uni-directional data flow. It controls derived data and enables communication between multiple components using a central Store which has authority for all data. Any update in data throughout the application must occur here only.
- Action => dispatcher => store => view => action => dispatcher ...
