https://www.patterns.dev/posts/
https://www.patterns.dev/posts/classic-design-patterns/#introduction

## **Design Patterns**

> Design patterns are a fundamental part of software development, as they provide typical solutions to commonly recurring problems in software design.

## Singleton Pattern

> Share a single global instance throughout our application

## Proxy Pattern

> Intercept and control interactions to target objects

## Provider Pattern

> Make data available to multiple child components(React Context API)

## Prototype Pattern

> Share properties among many objects of the same type

- The prototype pattern is a useful way to share properties among many objects of the same type. The prototype is an object that's native to JavaScript, and can be accessed by objects through the prototype chain.

## Container/Presentational Pattern

> Enforce separation of concerns by separating the view from the application logic

- In many cases, the Container/Presentational pattern can be replaced with React Hooks.

- With this pattern, we can separate the view from the application logic.
  - Presentational Components: Components that care about **how** data is shown to the user.A presentational component receives its data through props. Its primary function is to simply display the data it receives.
    Presentational components receive their data from container components.
  - Container Components: Components that care about **what** data is shown to the user. The primary function of container components is to pass data to presentational components,

## Observer Pattern

> Use observables to notify subscribers when an event occurs

- With the observer pattern, we can subscribe certain objects, the observers, to another object, called the observable.
- A popular library that uses the observable pattern is RxJS.

## Module Pattern

> Split up your code into smaller, reusable pieces

## Mixin Pattern

> Add functionality to objects or classes without inheritance

- A mixin is an object that we can use in order to add reusable functionality to another object or class, without using inheritance.

## Mediator/Middleware Pattern

> Use a central mediator object to handle communication between components

## HOC Pattern

> Pass reusable logic down as props to components throughout your application

## Render Props Pattern

> Pass JSX elements to components through props

## Hooks Pattern

> Use functions to reuse stateful logic among multiple components throughout the app

## Flyweight Pattern

> Reuse existing instances when working with identical objects

## Factory Pattern

> Use a factory function in order to create objects

- With the factory pattern we can use factory functions in order to create new objects. A function is a factory function when it returns a new object without the use of the new keyword!

## Compound Pattern

> Create multiple components that work together to perform a single task

## Command Pattern

> Decouple methods that execute tasks by sending commands to a commander
