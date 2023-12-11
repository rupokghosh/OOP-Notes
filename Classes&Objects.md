# Classes and Objects

A class is a blueprint or a template for creating objects. It defines the attributes (fields) and behaviors (methods) that objects of the class will have.

---
Syntax:
```java
public class Car {
    // Fields
    String make;
    String model;
    int year;

    // Constructor
    public Car(String make, String model, int year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }

    // Method
    public void startEngine() {
        System.out.println("Engine started!");
    }
}

```
### Objects

An object is an instance of a class.
It represents a real-world entity and encapsulates data and behavior.
```java
// Syntax: ClassName objectName = new ClassName();
Car myCar = new Car("Toyota", "Camry", 2022);

```

Accessing members
```java
// Accessing fields
System.out.println(myCar.make);

// Calling methods
myCar.startEngine();

```

---
### Instance Variables vs. Class Variables:

1. Instance variables belong to an instance of the class (each object has its own copy).
2. Class variables are shared among all instances of the class.

```java
public class MyClass {
    // Instance variable
    int instanceVar;

    // Class variable
    static int classVar;
}

```

---
### Constructors

Constructors are special methods used for initializing objects.
They have the same name as the class and do not have a return type.
Types:
- Default Constructor (no parameters)
- Parameterized Constructor (with parameters)

```java
// Default Constructor
public ClassName() {
    // Constructor body
}

// Parameterized Constructor
public ClassName(DataType parameter1, DataType parameter2) {
    // Constructor body
}
```

---
### Encapsulation

- The bundling of data (fields) and methods that operate on the data into a single unit (class).
- Access modifiers (public, private, protected) control access to the members of a class.