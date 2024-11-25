## Base

### Packages and classes

- https://docs.oracle.com/javase/8/docs/api/
- https://www.w3schools.com/java/java_ref_reference.asp
- https://www.javatpoint.com/java-tutorial
- https://www.youtube.com/@BroCodez

### Data Type

- Primitive Data Types
  - boolean, char, byte, short, int, long, float, double
- Non-Primitive Data Types
  - Class, Interface, Arrays, Enums

### Operators

Unary, Arithmetic, Shift, Relational, Bitwise, Logical, Ternary,Assignment .

### Keywords

abstract, class, if, etc.

### Variables

- String name = "John";
- int myNum = 15;

### Arrays

- String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

### Methods

- Overloaded methods - same name with different parameters
- Overriding - child class has the same method as parent class
- public - called by creating objects
- static - called without creating objects

```
static void myMethod(String fname) {
    System.out.println(fname + " Refsnes");
  }
```

## OOP

### Class

```
public class Main {

  // Attribute
  int x;

  // Constructor
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  // Method -
    static - can be accessed without creating an object of the class
    public - only be accessed by objects
  static void myMethod() {
    System.out.println("Hello World!");
  }
}
```

### Object

```
public class Main {
    int x = 5;

    public static void main(String[] args) {
        Main myObj = new Main();
        System.out.println(myObj.x);
    }
}
```

### Access Modifiers

- Private: only within the class. It cannot be accessed from outside the class.
- Default: only within the package. It cannot be accessed from outside the package.
- Protected: within the package and outside the package through child class.
- Public: everywhere.

### Encapsulation - "sensitive" data is hidden from users

- declare class variables/attributes as private
- provide public get and set methods to access and update the value

### Inheritance - class Car extends Vehicle

- subclass (child) - the class that inherits from another class
- superclass (parent) - the class being inherited from

### Polymorphism - single action in different ways

- Same method name different results in child classes.

### Abstraction - showing only essential information to the user

- Abstract class - cannot create objects, must be inherited
- Abstract method - used in an abstract class with no body.

### Interfaces - group related methods with empty bodies

```
// interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void run(); // interface method (does not have a body)
}
```

### Enums - group of constants

### Packages - group related classes

- Built-in Packages - https://docs.oracle.com/javase/8/docs/api/
- User-defined Packages -

### Iterator

- loop through collections, like ArrayList and HashSet.

### Lambda Expressions

- numbers.forEach( (n) -> { System.out.println(n); } );

### Data Structures

- Arrays
- ArrayList - resizable array
- LinkedList - use to manipulate data
- Stack
- Queue
- HashMap - store items in "key/value" pairs, for-each loop.
- HashSet - collection, every item is unique, for-each loop
- TreeSet
- TreeMap
- Graph
- Tree
