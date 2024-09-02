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

### React concept
- virtual DOM instead of the real DOM.
- It uses server-side rendering.
- One way data flow
- JSX
- Embedding expressions in JSX
- Declarative vs Imperative


### Building blocks of React
- **Components**: Reusable blocks of code that return HTML.
- **JSX**: It stands for JavaScript and XML and allows you to write HTML in React. By using JSX, we can write HTML structures in the same file that contains JavaScript code.
- **Props and State**: props are like function parameters and State is similar to variables.
- **Context**: This allows data to be passed through components as props in a hierarchy.
- **Virtual DOM**: 
    - lightweight representation of the 'real' DOM in the memory. When the state of an object changes, VDOM changes only that object in the real DOM instead of updating all of the objects. Synced with the real DOM by a library such as ReactDOM.
    - How it works:
        - React crate copy of the real DOM.
        - On component render, React creates Virtual DOM representation in memory.
        - On state or props change, React creates a new Virtual DOM representation.
        - Compares the new Virtual DOM with the previous one.
        - Updates the real DOM
    - How improve performance:
        - grouping multiple updates together before applying them to the real DOM
        - It only updates the specific components or elements that have changed

### Props and State
- **Props** pass data from one component to another. Objects which can be used inside a component. One way from parent to child. Props data is read-only, which means that data coming from the parent should not be changed by child components.

- **State** is local data storage. Object to keep some information about component. When the state object changes, the component re-renders.

### State vs. Props

||State|Props|
|:---|:---|:---|
Use|Holds information about the components|Allows to pass data from one component to other components as an argument
Mutability|Is mutable|Are immutable
Read-Only| Can be changed| Are read-only
Child components| Child components cannot access |Child component can access 


### Virtual DOM
- Lightweight copy of the actual DOM. Manipulating Virtual DOM is more faster.

### React Elements
     Elements are the building blocks for components. React apps usually have a single root DOM node in the HTML file, which is div id="root" and react DOM manages everything inside it. In order to render a react element in the root DOM node, both of them have to passed into ReactDOM.render().
- React Element Tags - h1, button
- React Element Attributes - className
- React Elements Embedded Javascript - className={divClass}
- React Element Inline Styles
    - style={{ color: 'blue', textAlign: 'center' }}
- React Fragments

### React Components - building blocks of web application.
    Components are functions that take inputs as props and return the elements for UI. There are two kinds of components:
    Class components and functional components but functional components are standard today.
- Functional Components(Stateless) - always produce the same output for the same input props and do not have any side effects. 
    - Javascript functions that return JSX.
    - No render method
    - No lifecycle methods
    - No Constructors
- Class(Stateful) - may produce different output for the same input props or have side effects.
-  Higher-order component
    - Takes the original component and returns the enhanced component. Helps to get rid of copying the same logic in every component. Acts as a container for other components.
- Pure Components
    - Pure components are the simplest and fastest components which can be written.
- Controlled Component - whenever a component is connected to a state, so that we can manage data, then its a controlled component. A controlled component allows Two Way Binding , where we both use and update its data programmatically.

### Stateful(Class) vs. Stateless(Functional) components.
||Stateful(Class) Component|	Stateless(Functional) Component|
|:---|:---|:---|
State| Can hold or modify state| Print out what is given to them via props
Simplicity|Complex as compared to the stateless component|Simple and easy to understand
Lifecycle methods|Can work with all lifecycle methods|Does not work with any lifecycle method
Reusability|Can be reused|Cannot be reused

### Hooks -  React version 16.8 
    Reusable functions that allows you to use state and other React features without writing a class.
    https://react-v8.holt.courses/lessons/hooks-in-depth/useref
https://tanstack.com
- useState
    -  store values scoped to a component. 
- useEffect 
    - create side effects in our component(action which is not related to current component).
- useLayoutEffect
    - identical to the useEffect hook except it runs immediately after DOM changes. This is useful if you need to make DOM mutations and don't want the screen to flicker between renders.
- useRef
    - like useState but doesn't rerender component if ref data is updated.Refer react element to the DOM element.
- useCallback 
    - memoize callbacks. Prevents functions recreated between re-renders.
- useMemo 
    - memoizes the return value
- useContext
    - access Context without need to use it’s Consumer component
- useReducer
    - Alternative to useState for managing more complex state logic. It accepts a reducer function and an initial state, returning the current state and a dispatch function to trigger state updates.
- custom hooks: normal JS functions start with "use". It helps us to write a logic once and use it anywhere in the code. Extract reusable logic.


### Lifecycle Methods
    Mount, Update, Unmount
- componentDidMount
- componentWillUnmount
- componentDidUpdate

### TailwindCSS

- TailwindCSS for css classes, grid/flex, etc.
- https://flowbite-react.com for UI components

### Lint, Prettier, Husky

https://medium.com/yavar/setting-up-a-eslint-prettier-husky-and-lint-staged-integration-with-typescript-in-next-js-13-14-68044dfae920

### Advanced React performance

- Code splitting
  https://bundlephobia.com
- SSR

### Optimize a React code?
- meaningful component names
- Break down components
- destructuring
- prop-types
- functional components
- Avoid using inline styles
- arrow functions
- spread operator


### Testing

https://nextjs.org/docs/app/building-your-application/testing/jest


https://github.com/sudheerj/reactjs-interview-questions#what-is-react

https://www.simplilearn.com/tutorials/reactjs-tutorial/reactjs-interview-questions

https://www.edureka.co/blog/interview-questions/react-interview-questions/
