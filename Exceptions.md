# Exceptions

Exceptions - an object that describes an unusual or erroneous situation. It is thrown by a program and may be caught and handled by another part of the program. ( An error is also represented as an object in Java ) 

A program can deal with an exception in three ways:

1. ignore it
2. handle where it occurs
3. handle it at another place in the program

If the exception is ignored, the program will terminate abnormally and produce a message with a call stack trace which indicates the line on which it occurred. It shows the method call trail that leads to the exception.

---
### Try Catch Statement

- The **`try`** block contains the code that might throw an exception.
- The **`catch`** block handles the exception if it occurs. Multiple catch blocks can be used to handle different types of exceptions.
- The **`finally`** block (optional) is always executed whether an exception is thrown or not. It is often used for cleanup operations.
```java
try {
    // code that may throw an exception
} catch (ExceptionType1 e1) {
    // handle ExceptionType1
} catch (ExceptionType2 e2) {
    // handle ExceptionType2
} finally {
    // optional cleanup code
}
```

---
### Exception Propagation

Exceptions propagate up through the method calling hierarchy until they are caught and handled or until they are caught or handled or until they reach the level of the main method. 

### The Exception Class Hierarchy

- All exceptions ( and errors ) in Java are derived from the base class **`Throwable`**.
- There are two main types of exceptions: checked exceptions and unchecked exceptions.
- Checked exceptions (e.g., **`IOException`**, **`SQLException`**) must be either caught in a try-catch block or declared in the method using the **`throws`** keyword.
- Unchecked exceptions (e.g., **`NullPointerException`**, **`ArrayIndexOutOfBoundsException`**) are not required to be caught or declared. The only unchecked exceptions in Java are objects of type `RuntimeException` or any of its descendants.
- Errors are similar to `RuntimeException` and its descendants in that:
    - errors should not be caught
    - errors do not require a throws clause

---
### The throw statement
- The **`throw`** keyword is used to manually throw an exception.
- The **`throws`** keyword is used in the method signature to declare that the method may throw certain exceptions.
```java
void method() throws MyException {
    // method code
    if (some condition) {
        throw new MyException("This is an exceptional situation");
    }
}
```

---
### I/O Exceptions

**`IOException`** is a checked exception that is thrown when an I/O operation fails or is interrupted. Common subclasses of **`IOException`** include **`FileNotFoundException`**, **`EOFException`**, and **`SocketException`**. It is thrown when: 

1. A file might not exist
2. Even if it exists, a program may not be able to find it
3. The file might not contain the kind of data we expect

### Standard I/O

- **`System.in`**: Standard input stream, typically connected to the keyboard. It is an instance of **`InputStream`**.
- **`System.out`**: Standard output stream, used for normal output. It is an instance of **`PrintStream`**.
- **`System.err`**: Standard error stream, used for error messages. It is also an instance of **`PrintStream`**.

### Writing Text Files

The `FileWriter` class represents a text output file but with minimal support for manipulating data. Therefore, we also use `PrintWriter` objects which have `print` and `println` methods. Output streams should always be closed explicitly.