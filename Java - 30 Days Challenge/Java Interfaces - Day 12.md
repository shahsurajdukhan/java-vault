Java interface is a collection of abstract methods.  The interface is used to achieve abstraction in which you can define methods without their implementations. An interface is a reference type and is similar to the class.

==🔴AN INTERFACE IS LIKE A CONTRACT OR A SET OF RULES THAT A CLASS AGREES TO FOLLOW==

Along with abstract methods, an interface may also contain constants, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods.

Writing an interface is similar to writing a class. However, a class describes the attributes and behaviors of an object. An interface contains behaviors that a class implements. Unless the class that implements the interface is abstract, all the methods of the interface need to be defined in the class.

## Java Interfaces and Classes - Similarities and Differences

### Similarities
- An interface can contain any number of methods
- An interface is written in a file with a .java extension, with the name of the interface matching the name of the file.
- The byte code of an interface appears in a .class file
- Interfaces appear in packages, and their corresponding bytecode file must be in a directory structure that matches the package name.

### Differences
- You cannot instantiate an interface
- An interface does not contain any constructors
- All the methods in an interface are abstract
- An interface cannot contain instance fields. The only fields that can appear in an interface must be declared both static and final.
- An interface is not extended by a class; it is implemented by a class.
- An interface can extend multiple interfaces

### Declaring an interface in Java
The **interface** keyword is used to declare an interface.

Ex: 
// File name : NameOfInterface.java
import java.lang.*;
// Any number of import statement

public interface NameOfInterface {
// Any number of final, static fields
// Any number of abstract method
declarations\
}

### Properties of Java Interface
- An interface is implicitly abstract. You do not need to use the abstract keyword while declaring an interface.
- Each method in an interface is also implicitly abstract, so the abstract keyword is not needed.
- Methods in an interface are implicitly public.

interface Animal {
public void eat();
public void travel();
}

### Implementing Interfaces in Java
When a class implements an interface, you can think of the class as signing a contract, agreeing to perform the specific behaviors of the interface. If a class does not perform all the behaviors of the interface, the class must declare itself as abstract.

A class uses the implements keyword to implement an interface. The implements keyword appears in the class declaration following the extends portion of the declaration.