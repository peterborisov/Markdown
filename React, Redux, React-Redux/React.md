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