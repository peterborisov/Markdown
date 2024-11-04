## Redux

#### 1. What is Redux?

- State management tool
- can be used with any JavaScript framework or library
- stores the state of the application, and the components can access the state from a state store

#### 2. What are the three principles that Redux follows?

- **Single source of truth:**
  - The state of the entire application is stored in an object/ state tree within a single store. So all the component’s state are stored in the Store and they receive updates from the Store itself.
- **State is read-only:**
  - The only way to change the state is to initiate an action, an object describing what happened.
- **Changes are made with pure functions**.
  - The user can return new state objects instead of mutating the previous state

#### 3. List down the components of Redux.

- **Action** – It’s an object that describes what happened.
  - Actions are payloads of information that send data from your application to your store.
  - Any data, whether from UI events or network callbacks, needs to eventually be dispatched as actions.
  - Actions must have a type field, indicating the type of action being performed.
- **Reducer** – Reducers are pure functions that takes the previous state and an action, and returns the next state.
  - describe, how the application's state changes.
  - A reducer is a function that accepts the current state and action, and returns a new state with the action performed.
  - combineReducers() utility can be used to combine all the reducers in the app into a single index reducer
- **Store** – Holds the state of the application.

  - getState() returns the current state of the store.
  - dispatch() dispatches an action. It is the only way to update the application state.
  - subscribe() subscribes a change listener to the state.
  - unsubscribe() is useful when you no longer want to call your listener method when the state changes.

- **View** – Simply displays the data provided by the Store.

#### 4. How are Actions defined in Redux?

- In Redux, actions are created using the functions called Action Creators.

```
//Action creator
function addTodo(text) {
       return {
                type: ADD_TODO, //action
                 text
    }
}
```

#### 5. Explain the role of Reducer.

- Reducers are pure functions which specify how the application’s state changes in response to an ACTION. Reducers work by taking in the previous state and action, and then it returns a new state. It determines what sort of update needs to be done based on the type of the action, and then returns new values. It returns the previous state as it is, if no work needs to be done.

#### 6. How is Redux different from Flux?

| Flux                                         | Redux                                      |
| :------------------------------------------- | :----------------------------------------- |
| 1. The Store contains state and change logic | 1. Store and change logic are separate     |
| 2. There are multiple stores                 | 2. There is only one store                 |
| 3. All the stores are disconnected and flat  | 3. Single store with hierarchical reducers |
| 4. Has singleton dispatcher                  | 4. No concept of dispatcher                |
| 5. React components subscribe to the store   | 5. Container components utilize connect    |
| 6. State is mutable                          | 6. State is immutable                      |

#### 7. What are the advantages of Redux?

- **Predictability of outcome** – Since there is always one source of truth, i.e. the store, there is no confusion about how to sync the current state with actions and other parts of the application.
- **Maintainability** – The code becomes easier to maintain with a predictable outcome and strict structure.
- **Server-side rendering** – You just need to pass the store created on the server, to the client side. This is very useful for initial render and provides a better user experience as it optimizes the application performance.
- **Developer tools** – From actions to state changes, developers can track everything going on in the application in real time.
- **Community and ecosystem** – Redux has a huge community behind it which makes it even more captivating to use. A large community of talented individuals contribute to the betterment of the library and develop various applications with it.
- **Ease of testing** – Redux’s code is mostly functions which are small, pure and isolated. This makes the code testable and independent.
- **Organization** – Redux is precise about how code should be organized, this makes the code more consistent and easier when a team works with it.

# React-Redux

## React Redux pattern

> Action creators, reducers, provide the store and connect to components.<br>
> Components can access state and dispatch actions.<br>

### Three Core Concepts

> **Store** - hold the state of application.<br>
> The store of whole app is stored in an object tree within a single store<br>

> **Action** - describes the changes in the state of the application.<br>
> The only way to change the state is to emit an action, an object describing what happened.

> **Reducer** carries out the state transition depending on the action.<br>
> To specify how the state tree is transformed by actions, you write pure reducers.<br>
> Reducer(previousState, action) => newState

### Actions

> The only way app can interact with the store.<br>
> Carry some info from app to the redux store.<br>
> Plain JS objects.<br>
> Have 'type' property that indicates the type of action being performed.(tipically string)<br>

**Action creator** is function that return action

```
const MY_ACTION = 'MY_ACTION';
const someAction = () => {
    return {
        type: 'MY_ACTION',
        info: 'First redux action'
    }
}
```

**Async Actions**

> Asynchronous API calls to fetch data from an end point and use that in application.

### Reducers

> Specify how the app's state changes in response to actions send to the store.<br>
> Function that accept state and action as arguments and returns the next state of the application.<br>
> Can declare multiple reducers.<br>
> CAn combine reducers.<br>

```
//(previousState, action) => newState

const initialState = {
    numOfItems: 10
}

const reducer = (state = initialState, action) => {
    switch(action.type){
        case MY_ACTION: return {
            //Make copy of state
            ...state,
            //And than update number of items
            numOfItems: state.numOfItems + 1
        }
        default: return state
    }
}
```

### Store

> One store for entire application.<br>
> Holds app state.<br>
> Allow access to state via getstate().<br>
> Allow state to be updated via dispatch(action)<br>
> Register listener via subscribe(listener)<br>

### Middleware

> Is the suggested way to extend Redux with custom functionality.<br>
> Provides a third-party extension point between dispatching an action and the moment it reaches the reducer.<br>
> Use middleware for logging, crash reporting, etc.<br>
> npm i redux-logger

- **Flux** - is an architectural pattern which enforces the uni-directional data flow. It controls derived data and enables communication between multiple components using a central Store which has authority for all data. Any update in data throughout the application must occur here only.

  - Action => dispatcher => store => view => action => dispatcher ...

- **Redux-saga** - handling side effects in redux app
- **Redux Thunk** - middleware that return a function instead of an action.
