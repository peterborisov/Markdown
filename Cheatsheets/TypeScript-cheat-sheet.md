### Cheat sheet https://zerotomastery.io/cheatsheets/typescript-cheat-sheet/

### Q&A https://zerotomastery.io/blog/typescript-interview-questions/

- https://www.javatpoint.com/typescript-tutorial
- https://www.freecodecamp.org/news/learn-typescript-beginners-guide/
- https://react-typescript-cheatsheet.netlify.app/docs/basic/getting-started/forms_and_events/
- https://github.com/typescript-cheatsheets/react

### Variables
    Named memory location that can hold a value

### Simple types
1. boolean
2. number
3. string
4. bigint
5. symbol
6. any
7. unknown
8. never
9. undefined and null

#### Type Assignment
- Explicit - define type: (let firstName: string = "Dylan";)
- Implicit - TypeScript will "guess" the type (let firstName = "Dylan";)

### Arrays
    Collections of values of the same type. 
- const names: string[] = [];
- **readonly** keyword can prevent arrays from being changed.

### Tuples
- A tuple is a typed array with a pre-defined length and types for each index.

```
let ourTuple: [number, boolean, string];
const graph: [x: number, y: number] = [55.2, 41.3];
```

### Object Types

```
const car: { type: string, model: string, year: number } = {
  type: "Toyota",
  model: "Corolla",
  year: 2009
};
```

### Functions

- Return Type - value returned can be explicitly defined
- Void Return Type - doesn't return any value
- Parameters
  - Optional Parameters => ?
  - Default Parameters => name: string = "Test"
  - Named Parameters
  - Rest Parameters
- Type Alias

### Control Flow
    Control flow allows programmers to control the flow of their code based on certain conditions or events. Control flow structures include conditional statements, loops, and function calls, which allow for branching and repetition of code.
### Repetition
    Repetition structures allow you to execute code repeatedly(loops)
### Classes
    Way to define blueprints for objects. They encapsulate data and behavior and can be used to create instances of objects with predefined properties and methods. 
```
class Person {
  name: string;
}

const person = new Person();
person.name = "Jane";
```

- Visibility
  -  public - (default) allows access to the class member from anywhere
  -  private - only allows access to the class member from within the class
  -  protected - allows access to the class member from itself and any classes that inherit it

### Interfaces
    Interfaces provide a way to define the shape of objects or classes. They define the contracts that objects must follow, specifying the properties and methods that an object must have.
```
interface Rectangle {
  height: number,
  width: number
}

const rectangle: Rectangle = {
  height: 20,
  width: 10
};

//Extending Interfaces
interface ColoredRectangle extends Rectangle {
  color: string
}

const coloredRectangle: ColoredRectangle = {
  height: 20,
  width: 10,
  color: "red"
};
```
### Enums - represents a group of constants

```
enum CardinalDirections {
  North = 'North',
  East = "East",
  NotFound = 404,
  Success = 200,
};
// logs "North"
console.log(CardinalDirections.North);
```

### Type Aliases
```
type Car = {
  year: number,
  type: string,
}

const myCar = {
 car: Car
};
```

### Maps
    A Map is a data structure that allows you to store data in a key-value pair format. Keys in a map must be unique, and each key can map to only one value. You can use any type of value as the key, including objects and functions, but strings and numbers are recommended to keep the map easy to work with.
### Exceptions
    Exceptions are a way to handle errors and unexpected behavior in your code. 
    Exceptions are thrown using the throw keyword and caught using the try...catch statement.
### Unions
    Variable or parameter that can hold multiple types.
    type Color = "red" | "green" | "blue";
    const red: Color = "red";
### Type Predicates
    Type predicates offer a way to determine the type of data based on a condition.
### Optional Chaining
    Optional properties are convenient because they allow situations where it may not be appropriate to have data present.

### Union Types - value can be more than a single type
  string | number | undefined

### Utility Types
    TypeScript provides handy utility types which are used to create new types from existing types.
```
interface UserForm {
  email: string;
  password: string;
}

// only properties:
type LoginForm = Pick<UserForm, "email" | "password" | "passwordConfirmation">;

// except:
type LoginForm2 = Omit<UserForm, "email">;

// mandatory
type SignupForm = Required<UserForm>;

// Cannot reassign any properties:
type SubmittedForm = Readonly<UserForm>;
```
### Casting

- Casting with:
  - as

```
let x: unknown = 'hello';
console.log((x as string).length);
```

  - <>

```
let x: unknown = 'hello';
console.log((<string>x).length);
```

  - Force casting

```
let x = 'hello';
console.log(((x as unknown) as number).length); // x is not actually a number so this will return undefined
```

### Async/Await
### Generic Functions
    They allow a type to be specified dynamically. Designed to work with different types of data.

  ```
  function getFirst<T>(arr: T[]): T | undefined {}

const nums = [1, 2, 3];
const one = getFirst(nums);  // T is `number`

const letters = ["a", "b", "c"];
const a = getFirst(letters);  // T is `string`

const objects = [{ first: 1 }, { second: 2 }];
const first = getFirst(objects);  // T is `object`
  ```

### Generic Classes
    Class that can work with a variety of different data types.
