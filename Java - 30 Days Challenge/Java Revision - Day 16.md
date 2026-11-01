1. What is Java - Java is a popular high-level, object oriented programming language developed by Sun Micro systems in 1995.
2. What is WORA in Java - WORA stands for Write Once Run Anywhere, this means that compiled java code can run on all platforms that support java without the need to recompile.
3. Different Features of Java - Object Oriented, Platform Independent, Easy to Learn, Secure, Architectural-Neutral, Portable, Robust, Multithreading, High performance, Distributed.
4. Different Applications of Java - Enterprise Solutions, Game development, Secure Web Development, Embedded Systems, Mobile Application development, Big Data Applications, and many more...
5. What is JVM - Java Virtual Machine is a virtual machine, an abstract computer that has its own ISA, Memory, Stack, Heap, etc. It runs on the host OS and places its demands for resources on it.
6. Types of Modifiers in Java - It is possible to modify classes, methods, etc.. by using modifiers. There are two categories of modifiers 1. Access Modifiers - default, public, protected, private. 2.  Non-access Modifiers - Final , abstract , strictfp
7. What is Java ENUMS - Enums restrict a variable to have one of only a few predefined values. The values in this enumerated list are called enums.
   for ex : if we consider an application for a fresh juice shop, it would be possible to restrict the glass size to small,medium, and large. This would make sure that it would not allow anyone to order any size other than small,medium, or large.
8. Types of Java Variables - there are 3 types 1. Local Variables 2. Instance variables 3. Class/Static variables

---
# Revision : Day1 to Day15

---

Day - 1 : HashSet - HashSet is a class in java used to store a collection of unique elements.
for this we have to import it. import java.util.Hashset; then `HashSet<String> names = new Hashset<> ();`

Hashset doesn't allow duplicates and it also doesn't maintain insertion order and it allows only one null value
Hashset calculates the object's hash code and this hashcode helps java determine where the object should be stored internally. for searching also it uses the hashcode.

---

Day - 2 :  Apache Kafka - this is a distributed event streaming platform used to send, receive , store and process large amounts of data in real time.
acts as a high-performance middle layer that allows different application/services to communicate with each other through streams of events or messages.
There is a producer which sends messages/events to kafka.
then there is a consumer which reads messages from kafka.
topic is a logical category where kafka stores events.
Broker is a kafka server, a kafka cluster can contain multiple brokers.
consumer group - multiple consumers can work together as a consumer group.

Adv. of Kafka - high throughput, scalability, fault tolerance, durability, real-time processing, loose coupling, message replay... etc...

---
gRPC - Day 3 

Google Remote Procedure Call - open-source protocol meant to enable flawless communication across dispersed systems.
RPC frameworks enables simple and effective communication between services.
it allows one application to call a method running on another application as if it were a local method.
GRPC works -
Client -> gRPC -> HTTP/2 Connection -> Server -> Business Logic
gRPC is particularly used in microservices architectures.
instead of every service communicating through REST/JSON , internal services can communicate through gRPC.
gRPC have performance, Language Support, Streaming,etc...
gRPC have cross-language support , Load Balancing, Pluggable Authentication ,etc...

---
JPA & Hibernate - Day 4

JPA is Java Persistence API - used to store Java Objects in a relational database. which allows us to work with database table using java objects instead of writing SQL for every operation.
JPA defines rules and interfaces for ORM
Hibernate is an implementation of JPA
> JPA defines the rules for connecting java objects with database table
> Hibernate implements the rules defined by JPA and handles the actual interaction with the databases.


---
Types of Classes in Java - Day 5

Conrete class - normal class whose objects can be created differently.
Abstract class - declared using abstract keyword.
Super class - superclass is a parent class while subclass is a child class that inherits from it using extends.
Object class - object is the root superclass of java's class hierarchy. Every class directly or indirectly inherits from it, unless it is a primitive type.
Nested class - a class declared inside another class. java supports these types of class
POJO Class
Enum class
Singleton class
Immutable class
Wrapper class

---
Exception Handling in Java - Day 6

for this we use try and catch - try statement allows us to define a block of code to be tested for errors while it is being executed.
catch statement allows us to define a block of code to be exectued, if an error occurs in the try block.
try and catch keywords always come in pairs.

Finally term is used to run by default regardless of which block is being executed try or block.
Finally statement let's us execute code after try..catch , regardless of the result : if the try block runs then also finally block will run and if the catch block will run then also the finally block will run.

Throw keyword is used to create a custom error, there are many types which can be used here like :
ArithmeticException, FileNotFoundException, ArrayIndexOutOfBoundException, SecurityException, etc...

---
Multithreading in Java - Day 7

Enables a program to run multiple threads simultaneously. allowing tasks to execute in parallel and utilize the CPU more efficiently. A thread is a lightweight, independent unit of execution inside a program.

ADV. of multi threading - Improved performance , Efficient CPU utilization , Responsiveness, Resource Sharing, Better User experience.

---
REST APIs in Java - Day 8

REST stands for representational state transfer. it is an architectural style for designing network APIs.
A REST APIs commonly uses HTTP to let a client, create, retrevie, update and delete resources.
GET - used to retreive the data
POST - used to create a reosource
PUT - used to replace/ update a resource
PATCH - used to partially update a resource
DELETE - used to delete a resource

JSON is javascript object notation . lightweight format for exchanging data between applications.
Spring boot uses the jackson library to convert java objects to JSON and JSON to java objects.
Serialization : java objects -> JSON
Deserialization : JSON -> Java Objects

---
Collection Framework in Java - Day 9

JCF - is java collection framework used in real-world application development, is a set of interfaces, classes, and algorithms that help us store, organize, access, search and manipulate group of objects.

ex: an array has a fixed size with an arraylist you can add on dynamic timings...

To store multiple objects without manually managing array sizes
to add , remove, search and update elements easily
to remove duplicates when needed
to store data as key value pairs
to sort and process data efficiently
to choose different data structures for different requirements

---
Java Features and Java Applications - Day 10

java is a feature rich language - it has object oriented , platform independent, easy to learn, secure, architectural neutral , portable , robust , multithreading, high performance , distributed
Java Applications - Enterprise solutions, Game development, secured web development, embedded systems, mobile application development, big data applications, and many more....

---
Java Constructors - Day 11

java constructors are special types of methods that are used to initialize an object when it is created. however constructors have no explicit return type.
the name of the constructors must be same as the class name.
all classes have constructors, whether we define or not because java automatically provides a default constructor that initializes all member variables to zero.
java constructors do not have a return type , don't use void as a return type.

3 types of java constructor
- default constructor - java provides a default constructor that initializes the object
- No-Args constructor - no-arg does not accept any argument.
- Parameterized constructor - a constructor with one or more than one arguments
constructor overloading - means multiple constructors in a class. when you have multiple constructors with different parameters listed, then it will be known as constructor overlaoding.

---
Java Interfaces - Day 12

java  interfaces is a collection of abstract methods. the interface is used to achieve abstraction in which you can define methods without their implementations. an interface is a reference type and is similar to the class.

along with abstract methods, an interface may also contain constants, default methods, static methods, and nested types. method bodies exist only for default methods and static methods.

An interface is implicitly abstract, we do not need to use the abstract keyword while declaring an interface.
each method in an interface is also implicitly abstract, so the abstract keyword is not needed.
methods in an interface are implicitly public.

---
Java File Handling - Day 13

Reason why we use file handling is that when our program terminates, the values stored in these variables are lost. what if we want to store this information permanently?
that's where file handling comes in.
Even after closing your java application or restarting your computer, the data remains stored.


java provides several methods for file handling like creating, updating, and deleting the files.

imagine your computer has a folder called documents containing a file named notes.txt the file class lets java refer to that file or folder and perform certain operations on it.

import java.io.file;
File myobj =  new File("filename.txt");

methods of the file class
- getName() - returns the file or directory name
- getPath()
- exists()
- createNewFile()
- delete()
- isFile()
- isDirectory()
- length()
- mkdir()
- list()


## Reasons why we use file handling
- Permanent storage
- Data retrieval
- Data modification
- Data Sharing
- Logging
- backup
- Configuration

EX: 
- Banking application
- student management system
- E-commerce application
- Attendance system
- Chat application
- Software application
all these applications need some form of persistent storage







---
  ## Complete Guide to File Handling - Day 14

#### Types of File Handling Operations
Java supports several common file operations.
1. Create - Create a new file
2. Read - Retrieve file data
3. Write - Store data in a file
4. Append - Add data at the end
5. Update - Modify existing data
6. Delete - Remove a file


#### Types of File Handling in Java
Java provides different file-handling approaches depending on the type of data you want to store.

Text file (Human Readable characters) - Binary file (Raw bytes)

Type 1 : Text File Handling - text files store information in a human-readable format.
EX : 
.txt
.csv
.json
.xml

Java uses character streams to handle text data.

FileReader - reads characters
FileWriter - writes characters
BufferedReader - Reads text efficiently using buffering
BufferedWriter - Writes text efficiently using buffering
PrintWriter - Writes formatted text

Type 2 : Binary File handling - Binary files store data in the form of bytes rather than directly readable text.
EX:
Images (.jpg , .png)
Audio (.mp3)
Videos (.mp4)
PDF Files
Executable files

Java uses byte streams to handle binary data.

Important classes :
FileInputStream - Reads bytes from a file
FileOutputStream - Writes bytes into a file
BufferedInputStream - Reads bytes efficiently using buffering
BufferedOutputStream - Writes bytes efficiently using buffering
DataInputStream - Reads primitive java data types
DataOutputStream - Writes primitive java data types
ObjectInputStream - Reads serialized objects
ObjectOutputStream - writes serialized objects


---
Java Thread Synchronization - Day 15


when two or more threads run within a program , there may be a situation when multiple threads try to access the same resource and finally they can produce unforeseen result due to concurrency issues. 

Java programming language provides a very handy way of creating threads and synchronizing their task by using synchronizd blocks. you keep shares resources within their block.

there is block synchronization too then there is Static synchronization where if a thread is in the static synchronized region, all other threads trying to access this region will be blocked. since static methods belong to the class therefore, static synchronization applies class level lock.