Java constructors are special types of methods that are used to initialize an object when it is created. it has the same name as its class and is syntactically similar to a method. However, constructors have no explicit return type.

typically we use a constructor to give initial values to the instance variables defined by the class or to perform any other start-up procedures required to create a fully formed object.

All classes have constructors, whether you define one or not because Java automatically provides a default constructor that initializes all member variables to zero. However, once you define your constructor, the default constructor is no longer used.

### Rules for creating java constructor 
- The name of the constructors must be the same as the class name.
- Java constructors do not have a return type. Even do not use void as a return type.
- There can be multiple constructors in the same class, this concept is known as constructor overloading.
- The access modifiers can be used with the consturctors, use if you want to change the visibility/accessibility of constructors.
- Java provides a default constructor that is invoked during the time of object creation. if you create any type of constructor, the default constructor is not invoked.

### Creating a Java Constructor
to create a constructor in java, simply write the constructor's name (same as the class name) followed by the brackets and then write the constructor's body inside the curly braces.

### Types of java constructor
3 different types of constructors in Java
- Default Constructor
- No-Args Constructor
- Parameterized Constructor

Default construtor - if you do not create any constructor in the class, Java provides a default constructor that initializes the object.

No-Args Constructor - As  the name specifies, the no-arg constructor does not accept any argument. By using the No-args constructor you can initialize the class data members and perform various activities that you want on object creation.

Parameterized Constructor - a constructor with one or more arguments is called a parameterized constructor, most often we need a constructor that accepts one or more parameters, parameters are added to a constructor in the same way that they are added to a method, just declare them inside the parentheses after the constructor's name.

### Constructor overloading in Java
Constructor overloading means multiple constructors in a class. when you have multiple constructors with different parameters listed, then it will be known as constructor overloading.