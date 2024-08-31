### JavaScript Engine
- The Parser
- The AST - Abstract Syntax Tree
- The Interpreter:
    - Executes each line of code line by line, without requiring them to be compiled into a machine language program.
- The Compiler:
    - Babel
    - Typescript 
- The Combo
### Writing Optimized Code
- Memoization - cache a return value
- Inline Caching
- Hidden Classes
- Managing Arguments
### Call Stack and Memory Heap
- Memory Heap - store and write information
- Call Stack - The call stack keeps track of where we are in the code, so we can run the program in order. Things are placed into the call stack on top and removed as they are finished.
### Stack Overflow
- Garbage Collection
- Synchronous - only one thing can be done at a time
- Event Loop - When you run some JavaScript code in a browser, the engine starts to parse the code. Each line is executed and popped on and off the call stack.
- Callback queue - cannot be ran until the call stack is completely empty. 
- Job Queue
- 3 Ways to Promise
- Threads, Concurrency, and Parallelism
### Execution Context
-  Execution context is simply the environment within which your code is ran.
    - 2 types: global or function.
    - 2 stages: the creation and executing phase.
- Global Execution Context
    - global object created, initializes "this" keyword to global, hoisting
- Function Execution Context
- Arrow Functions
### Hoisting
- Process of putting all variable and function declarations into memory during the compile phase.
### Lexical Environment
- created when curly brackets {} are used
### Scope Chain
- Each environment context that is created has a link outside of its lexical environment called the scope chain. The scope chain gives us access to variables in the parent environment.
### Function and Block Scope
### IIFE - Immediately Invoked Function Expression
### This
- Lexical vs Dynamic Scope
### Call, Apply, Bind
- Call
- Apply
- Bind
- Currying with bind
    - Currying is breaking down a function with multiple arguments into one or more functions that each accept a single argument.
### JavaScript Types
- Objects in JavaScript
- Primitive 
    -  passed by value, meaning their values are copied and then placed somewhere else in the memory. They are also compared by value. There are currently 7 primitive data types in JavaScript.
-  Non Primitive
    - passed by reference, meaning their properties are not stored separately in memory.
- Type Coercion
    - converting one type of value into another. There are 3 types of conversion in JavaScript.
        - to string
        - to boolean
        - to number
- Static vs Dynamic Typed
    -  when the types of variables are checked.
### The 2 Pillars: Closures and Prototypes
- Function Constructor
- Prototypal Inheritance - The child of the object "inherits" properties from its parent.
- Prototype vs proto
- Callable Object
- Higher Order Functions - takes a function as an argument or returns another function. 
    - There are 3 kinds of functions in JavaScript.
        - function ()
        - function (a,b)
        - function test() { return function () {} }
- Closures - gives you access to its outer functions scope from the inner scope.
- Memory Efficient
- Encapsulation
    - Restriction of direct access to some of an object's components. It hides as much as possible of an object's internal parts and only exposes the necessary parts to run. Why use encapsulation?
### Object Oriented Programming vs Functional Programming
- Object Oriented Programming -  all code should be grouped into "boxes" (objects) to make your program easier to read and understand.
- Factory Functions
- Stores
- Object.create
- Constructor Functions
- Class - not true classes, they are syntactic sugar. Under the hood, it is still using the old prototype method. 
- Private and public fields
### Functional Programming - Instead of objects, it uses reusable functions
    - Once something is created, it should not be changed, being immutable.
    - Unlike OOP, shared state is avoided as functional programming works on the idea of pure functions.
- Pure Functions - no side effects, same input return same output value. 
- Referential transparency
- Idempotence
- Imperative vs Declarative
    - Imperative programming: tells the computer what to do and how to complete it.
    - Declarative programming: tells the computer what to do, but not how to do things.
- Immutability 
    - ot modifying the original data or state. Instead we should create copies of the state inside our functions and return a new version of the state.
- Partial Application
- Pipe and Compose
- Arity
### Composition vs Inheritance
    - Composition is what we just did with FP, creating small reusable functions to make code modular.
    - Inheritance is what we did with OOP, creating a class and extending it to subclasses that inherit the properties.
- OOP Problems
- Finally
### Modules in JavaScript
    Modules are pieces of code, grouped together, that can be combined together to create an expandable program that can get bigger as it needs to.

- Module Patterns
    -  Before ES6 we had 2 ways to implement modules in JavaScript CommonJS and AMD.
- Issues With Modules
- ES6 Modules
    -  import and export keywords in our files to implement modules. 
### Error Handling
    Writing your programs you have the ability to use the throw keyword to stop the program and handle an error by using a try/catch block that has an optional finally block or the .catch() method for asynchronous code.
### Data Structures & Algorithms
    A data structure is different types of containers that hold your data. Each container has its own type of data it holds and is specific to that type. 
- How do computers work?
- Popular Data Structures
    - There are many implementations of data structures out there but there are only 2 fundamental kinds:
        -  array of contiguous memory locations 
        -  linked structures.
- Arrays
- Implementing an Array
- Hash tables
- Hash Collisions
- Hashing in JavaScript
- Create a Hash Table