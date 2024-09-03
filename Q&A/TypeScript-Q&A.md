## Beginner Typescript Interview Questions

#### What is TypeScript, and how does it differ from JavaScript?
    TypeScript is a statically typed superset of JavaScript that compiles down to plain JavaScript. Developed by Microsoft.
- Key differences between TypeScript and JavaScript include:
    - Static Typing: JS is dynamically(run-time) typed, TypeScript is static(compile-time) typing.
    - Interfaces and Classes: TypeScript supports the latest JavaScript features, such as classes and interfaces, which are not available in some older JavaScript versions
    - Compile-time Errors vs JS runtime
    - Tooling: TypeScript has powerful tools for navigating code and automatic refactoring, which improves developer experience
#### What are the main components of TypeScript?
- There are three main components in TypeScript
    - Language: types, annotations, classes, interfaces, tuples, etc. These additions enhance JavaScript.
    - The TypeScript Compiler: transpile TS  into JavaScript. It catches errors at compile time and enforces type-checking
    - The TypeScript Language Server
####  What are the main benefits and disadvantages of using TypeScript?
- Benefits 
    - Static Typing
    - Improved Readability and Maintainability
    - Easier Navigation through the code
    - Early Error Detection
    - Familiar Syntax for OOP Developers
- Disadvantages 
    - Learning Curve
    - More Complexity
#### What are interfaces in TypeScript?
- Define how our object need to look like.
#### Can you explain the concept of modules in TypeScript?
    File containing variables, functions, classes, etc. The key difference is all are private by default in TypeScript.
#### What is a TypeScript decorator and what is its purpose?
    They can be used to modify classes, methods, and properties.
```
function log(target: Function) {
  console.log(`${target.name} - has been logged`);
}

@log
class MyClass {}
```
#### Access modifiers
- public -  visible everywhere, and it's the default access level for class members.
- private - only accessible within the class that declares them.
- protected - private members,but can also be accessed within subclasses.

## Intermediate Typescript Interview Questions
#### What is ‘type inference’ in TypeScript?
    Automatic detection of the data type
    let x = 10; // `x` is inferred to have the type `number`
#### What are type guards in TypeScript?
     Way to provide additional information about the type.
     Type guards can be simple typeof or instanceof checks.

#### Difference between type and interface
    If you want to create complex type combinations, use type. If you're describing object shapes, interface is usually the better choice.
- type
    - supports union (|), intersection (&), typeof, etc, which allows you to create more complex types.
    ```
    type User = {
        name: string;
    } & {
        age: number;
    };

    let user: User = {
        name: 'John Doe',
    age: 30,
    };
    ```
- interface
    - can be merged
    ```
    interface User {
        name: string;
    }

    interface User {
        age: number;
    }

    let user: User = {
        name: 'John Doe',
        age: 30,
    };
    ```
#### Method overloading
     Multiple methods with the same name but different parameters or types. 
#### Mapped types
     Generic type which uses a union created from another type (usually an interface) to compute a set of properties for a new type.
####  index types
    The indexed access operator is used to access the property type of a specific type:
    type PersonNameType = Person['name'];

## Advanced Typescript Interview Questions
#### How do you use TypeScript with external libraries that don't have type definitions?
     Declare file with a .d.ts extension
#### Type intersection
    Combine multiple types into one.
    
## How did you do?
## BONUS: More TypeScript tutorials, guides & resources