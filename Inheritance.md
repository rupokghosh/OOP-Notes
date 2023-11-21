# Inheritance


Inheritance - is a fundamental concept in object-oriented programming (OOP) that allows a class (subclass/child) to inherit properties and behaviors from another class (superclass/parent). It creates an is-a relationship.\

---
### Why Inheritance?
1. Code reusability: Inherited classes can reuse the fields and methods of the parent class.
2. Extensibility: New functionalities can be added to the subclass without modifying the parent class.

### Declaration:

```
class Subclass extends Superclass {
    // subclass members
}
```
### Access Modifiers in Inheritance ( 4 Types)

- Public - these are accessible in the subclass. 
- Protected - these are accessible in the subclass and package. 
- Default (Package-Private) - only accessible within the same package. 
- Private - these are not directly accessible in the subclass. 

---
### The Super Keyword:
- Used to call the methods of the superclass.
- Used to invoke the superclass constructor since constructors are not inherited. 

```
class Subclass extends Superclass {
    @Override
    void display() {
        super.display(); // Calling the superclass method
        System.out.println("Subclass");
    }
}
```

--- 
### Types of Inheritance 
1. Single Inheritance - Java supports single inheritance, meaning that a derived class can have only one parent class. 
2. Multiple Inheritance - Multiple Inheritance allows a class to be derived from two or more classes, inheriting the members of all parents. 
It is NOT supported in Java. 

We can, however, use interfaces, which gives us aspects of multiple inheritance without the overhead. 

---
### Overriding Methods 
A child class can override the definition of an inherited method in favor of its own. 
It must have the same signature as the parent’s method, but can have a different body. 

```
class Superclass {
    void display() {
        System.out.println("i like cricket!");
    }
}

class Subclass extends Superclass {
    @Override
    void display() {
        System.out.println("i like football!");
    }
}
```
A method cannot be overiden if its declared with the final modifier. 

A method in the parent class can be invoked explicitly using the super reference.

### Overloading Methods
Multiple method with the same name in the same class but with different signatures. 
It lets you define a similar operation in different ways for different parameters. 