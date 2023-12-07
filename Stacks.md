# Stacks

A collection is an object that holds and organizes other objects. Some collections and linear in nature, others are non-linear. 

---
Stack - is a linear collection whose elements are added in a last in, first out ( LIFO ) manner. This means the last element to be put on a stack is the first one to be removed ( like a stack of books where you add and remove from the top )

Some important stack methods:

- The **`push`** method adds an element to the top of the stack.
- The **`pop`** method removes and returns the element at the top of the stack.
- The **`peek`** method returns the element at the top of the stack without removing it.
- The **`isEmpty`** method checks if the stack is empty.
- The `**size`** determines the number of elements on the stack.

---
### Generics

Generics are used to provide better type management control at compile-time and simplify the use of collection classes. Type parameters are specified in angle brackets (**`<>`**) after the class name.

**When should exceptions be thrown from a collection class?** 

Only when a problem is specific to the concept of the collection ( not its implementation or its use ). The user does not need to worry about it getting “full” but a stack should throw an exception if the user attempts to pop an empty stack. 

**How do we manage the capacity when we implement an array with stacks?**

The number of cells in an array is called its capacity. It's not possible to change the capacity of an array in Java once it's been created. Therefore, to expand the capacity of the stack, we'll create a new (larger) array and copy over the elements. This will happen infrequently, and the user of the stack need not worry about it happening. 

**Creating an array of a generic type:**

You cannot instantiate an array of a generic type directly. Instead, create an array of Object references and cast them to the generic type. 

**Defining an exception:**

An EmptyCollectionException is thrown when a pop or a peek is attempted and the stack
is empty. The EmptyCollectionException is defined to extend RuntimeException. By passing a string into its constructor, this exception can be used for other collections as well. 

---