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

  // Class attribute
  int x = 5;

  // Class method - static or public
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

### Encapsulation - "sensitive" data is hidden from users

### Inheritance

- subclass (child) - the class that inherits from another class
- superclass (parent) - the class being inherited from

### Polymorphism - single action in different ways

### Abstraction - showing only essential information to the user

### Access Modifiers

- Private: only within the class. It cannot be accessed from outside the class.
- Default: only within the package. It cannot be accessed from outside the package.
- Protected: within the package and outside the package through child class.
- Public: everywhere.

### Data Structures

- Arrays
- ArrayList
- LinkedList
- Stack
- Queue
- HashMap
- HashSet
- TreeSet
- TreeMap
- Graph
- Tree
