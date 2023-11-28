# Polymorphism

Polymorphism - The ability of a method to do different things based on the object that it is acting upon.

---
### What is Dynamic Binding / Late Binding?
Java defers method binding until run time.

### Benefits of Polymorphism:
1. Code Flexibility
2. Code Reusability
3. Easy to Maintain

### Types of Polymorphism:

- Compile-time Polymorphism ( Method Overloading )
    - Multiple methods with the same name but different parameters or types.
    - Decided at compile-time based on method signatures.

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```

- Runtime Polymorphism ( Method Overriding )
    - A subclass provides a specific implementation for a method that is already defined in its superclass.
    - Decided at runtime based on the actual object type.
```java
class Animal {
    void makeSound() {
        System.out.println("Some generic sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}
```    

---
### Interfaces

Interface - a collection of abstract methods and constants. It is used to establish a set of methods that a clas will implement. It provides a way to achieve multiple inheritance in Java. 
```java
interface Doable {
    void doThis();
}
```

### Things to know about Interfaces: 

1.  interface cannot be instantiated. 
2. Merthods in an interface have public visibility by default.
3. If a class states that it implements an interfact, it must define all methods in the interface. 
4. Interfaces can contain constants, which are implicitly public, static, and final. They are used to define values that should not be changed.
5. A class that implements an interface can implement other methods and other interfaces as well. This allows a class to inherit from more than one type. ( Multiple Inheritance )
```java
class Circle implements Interface1, Interface2 {
    // Class implementation
}
```

---
### The Comparable Interface
It contains a single method, **`compareTo(Object obj)`**, which is implemented by the class to provide the ordering logic.

**Implementing Comparable:**

- To make a class objects comparable, the class must implement the **`Comparable`** interface and provide the **`compareTo`** method.
```java
public class Person implements Comparable<Person> {
    private String name;
    private int age;

    // Constructor, getters, setters...

    @Override
    public int compareTo(Person otherPerson) {
        // Compare based on age
        return Integer.compare(this.age, otherPerson.age);
    }
}
```
**Sorting Collections:**

- Classes that implement **`Comparable`** can be easily sorted using methods like **`Collections.sort()`**.
```java
List<Person> people = new ArrayList<>();
// Add Person objects to the list
Collections.sort(people); // Uses the compareTo method for sorting
```

---
### The Iterator Interface

The **`Iterator`** interface in Java provides a way to iterate over a collection of objects.

It contains methods like **`boolean hasNext()`, `remove()`** and **`E next()`**.

The methods:

- The **`hasNext()`** method returns a boolean value (**`true`** or **`false`**) indicating whether there are more elements in the iteration. It is typically used in a loop to check if there are more elements before attempting to retrieve the next one.
- The **`next()`** method returns the next element in the iteration.It advances the iterator to the next position in the collection.
- The **`remove()`** method removes the last element returned by the **`next()`** method from the underlying collection.
- The enhanced for loop (also known as the "for-each" loop) provides a concise way to iterate over elements in a collection. The enhanced for loop is read-only; it cannot be used to modify the collection during iteration. It is particularly useful when the order of elements is not critical, such as when iterating through a set or a list where order doesn't matter.