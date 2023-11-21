## Inheritance

Inheritance - is a fundamental concept in object-oriented programming (OOP) that allows a class (subclass/child) to inherit properties and behaviors from another class (superclass/parent). It creates an is-a relationship.
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