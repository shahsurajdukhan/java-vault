Mainly 10-12 types of classes are present in Java
###### 1. Concrete Class 
    - A conrete class is a normal class whose objects can be created directly.
    - It provides implementations for its required methods.
    - for any concrete class, we can create it's object using `new`
###### 2. Abstract Class
   - Abstact class is declared using the abstract keyword.
   - You can't create it's object directly.
   - It can contain both abstract methods(without a body) and concrete methods (with a body).
   - It is used to define common behavior that subclass must or can implement.
###### 3. Super Class & Sub Class
- A superclass is a parent class, while a subclass is a child class that inherits from it using `extends.`
- mainly used to reuse existing code and create relationships between classes.
###### 3. Object Class
   - Object is the root superclass of Java's class hierarchy. Every class directly or indirectly inherits from it, unless it is a primitive type.
###### 3. Nested Class - A class declared inside another class. Java supports several forms.
	   - Inner Class (Non static Nested Class)
	   - Anonymous inner class
	   - Member inner class
	   - Local inner class
	   - Static Nested Class / Static class
4. Generic class
   - a class that works with any data type specified at compile time using type parameters like <T>.
4. POJO class
   -  (Plain old java object) - A simple class used strictly as a data container. it has private fields, default constructors, and public getters/setters, without implementing external frameworks or enterprise interfaces.
4. Enum class
   - a specialized class used to represent a fixed set of constants.
4. Singleton class
   -  a class designed to ensure that only instance can ever exist throughout the application runtime.

4. Immutable class
   - a class whose state (data inside its field) cannot be changed once created.
4. Wrapper class
   - primitive data types (int ,char, double ) are not objects. wrapper classes turn these primitives into full java objects (Integer, Character, Double).

---
## What is Class?
- A class is a blueprint or a template for creating objects, which are instances of the class.
- A class contains variables and methods that define the behavior and state of objects created from it.
- A class can have fields (variables), constructors, and methods.
- Fields are used to hold data or state, constructors are used to create objects, and methods are used to perform actions or operations on objects.
---
Concrete class example
- fully implemented class . you can create instances (objects) directly using new.

class Car {

	void drive () {
		system.out.println("Car is moving");
		}
}

Car myCar = new Car(); // allowed.

---
Abstract class - a blueprint that cannot be instantiated directly using new. it acts as a base class and can have incomplete methods (abstract methods) that subclass must complete.

ex: 

abstract class Animal {
	abstract void makeSound(); // no body, must be implemented by subclass
	void sleep() {
		System.out.println("Sleeping...");
	}
}

class Dog extends Animal {
@override
void makeSound(){
System.out.println("Woof!");
}
}

//usage
// Animal a = new Animal(); // error! cannot instantiate abstract class
Animal myDog = new Dog(); // this is allowed via subclass

---
Super class and sub class...
this describes a parent-child relationship via inheritance (extends)


EX:

class Vehicle {
	 int speed = 60;
}

class Bike extends Vehicle {
	void showSpeed() {
		System.out.println("Speed is:  " + speed); // inherits speed field
	}
}

---
Object class (Java.lang.Object)
the root of all classes in java. every class automatically extends object if it doesn't explicitly extend another class. it provides default methods like toString() , equals(), and hashCode().

Ex:

class Student() {
	// implicitly extends java.lang.object
}

Student s = new Student ();
system.out.println(s.toString()); // inherited directly from object class.


---
Nested classes - classes declared inside another class to logically group code or hide details.

Ex:

class OuterClass {

// 1. member inner class requires an instance of outerclass
class InnerClass {
	void display() {System.out.println("Inside Inner"); }
}

// 2. static nested class - does not require an instance of outer class
static class StaticNestedClass {
	void display() {System.out.println("Inside static nested"); }
}

void myMethod() {
// 3. Local inner class - declared inside a method
class LocalInnerClass {
	void greet() {System.out.println("Inside Local");}
}
LocalInnerClass local   = new LocalInnerClass();
local.greet();
}

}


Anonymous Inner class - a class without a name,declared and instantiated in a single expression. often used to override a method on the fly.

Ex:

interface Greeting {
		void sayHello();
}

public class Main {
public static void main (String[] args) {
//anonymous class implementing greeting on the spot
Greeting g = new Greeting() {
@override
public void sayHello() {
System.out.println("Hello from anonymous class!");
}
};
g.sayHello();
}
}


---
Generic Class - a class that works with any data type specified at compile time using type parameters like <T>.

Ex:
class Box<T> {
	private T value;

	public void set(T value) { this.value = value; }
	public T get() {return value; }
}

// usuage:
Box<String> stringBox = new Box<>();
stringBox.set("java");

Box<integer> intBox = new Box<>();
intBox.set(100);

----
Enum class - a specialized class used to represent a fixed set of constants.

Ex:
 enum Status {
	 PENDING, SUCCESS, FAILED
	 }
//USAGE:
		Status currentStatus = Status.SUCCESS;

---
Wrapper Class - primitive data types (int ,char, double ) are not objects. wrapper classes turn these primitives into full java objects (Integer, Character, Double).

Ex: 

int primitiveNum = 5;
Integer wrappedNum = Integer.valueof(primitiveNum); //autoboxing allows: integer wrappedNum = 5;

//Required for collections:
ArrayList<Integer> numbers = new ArrayList<>(); // cannot use ArrayList<int>


---
POJO Class (Plain old java object) - A simple class used strictly as a data container. it has private fields, default constructors, and public getters/setters, without implementing external frameworks or enterprise interfaces.

Ex:

public class User {
private String name;
private int age;

public User () {} // default constructor

public string getName() { return name; }
public void setName(String name) { this.name = name; }

public int getAge( ) {return age;}
public void setAge(int age) {this.age = age; }
}

---
Singleton Class - a class designed to ensure that only instance can ever exist throughout the application runtime.

Ex: 

class DatabaseConnection {
// 1. private static instance
private static DatabaseConnection instance;

//2. Private constructor prevents new DatabaseConnection() outside
private DatabaseConnection() {}

//3. Public static method to retrieve the single instance
public static DatabaseConnection getInstance( ) {
if (instance == null) {
	instance = new DatabaseConnection();
}
return instance;
}
}


---
Immutable Class - a class whose state (data inside its field) cannot be changed once created.

Ex: 

public final class Account {
	private final String accountNumber;

	public Account(String accoutNumber) {
		this.accountNumber = accountNumber;
	}


// only getter provided, No setter
public String getAccoutNumber () {
	return accountNumber;
}
}


---
So yeah, this is the in-depth study of Classes in java. 
for any queries reachout to me at suraj.adi@outlook.com  Thanks.