Multithreading in java is a feature that enables a program to run multiple threads simultaneously, allowing tasks to execute in parallel and utilize the CPU more efficiently. A thread is a lightweight, independent  unit of execution inside a program (process).

- threads allow parallel execution of tasks.
- A process can have multiple threads.
- each thread runs independently but shares the same memory.

EX: imagine a restaurant kitchen. multiple chefs (threads) are preparing different dishes at the same time. this speeds up service and utilizes all available resources (CPU).

# there are ways to create threads

1. Extending the thread class - we create a class that extends thread and override its run() method to define the task. then we make an object of this class and call start(), which automatically calls run() and begins the thread's execution.
Ex: Restaurant kitchen (extending thread)

class CookingTask extends Thread {
private String task;

CookingTask (String task) {
this.task = task;
}

public void run() {
System.out.println (task  + "is being prepared by " + Thread.currentThread().getName());
}
}

public class Restaurant {
public static void main (String[ ] args) {

thread t1 = new CookingTask ("Pasta");
thread t2 = new CookingTask ("salad");
thread t3 = new CookingTask ("Dessert");
thread t4 = new CookingTask ("Rice");


t1.start();
t2.start();
t3.start();
t4.start();


}
}


// Output - Rice is being prepared by thread 3
pasta is being prepared by thread 0
dessert is being prepared by thread 2
salad is being prepared by thread 1


- we created multiple threads (t1 - t4) using the CookingTask class
- each thread represents a dish being prepared
- calling start() creates a new thread with it's own call stack and internally invokes the run() method. this allows threads to run concurrently with the main thread and each other.

2.  Implementing the Runnable interface -
   we create a new class which implements  java.lang.runnable interface and define the run() method there. then we instaniate a thread object and call start() method on this object.
Ex :  Restuarant kitchen (Runnable interface)
class CookingJob implements Runnable {
private String task;

CookingJob (String task) {
this.task = task;
}

public void run() {
System.out.println (task + "is being prepared by " + Thread.currentThread().getName());
}
}

public class RestaurantRunnable {
public static void main(String[] args) {
 Thread t1 = new Thread (new CookingJob("Soup"));
 thread t2 = new Thread (new CookingJob("Pizza"));
 thread t3 = new Thread (new CookingJob("Burger"));

t1.start();
t2.start();
t3.start();
}
}

output /// 

Burger is being prepared by thread-2 
Pizza is being prepared by thread-1
Soup is being prepared by thread-0

explaination : CookingJob implements Runnable and overrides run().
we pass a Runnable object to the Thread constructor.
calling start() starts a new thread and invokes its run() method. the thread runs independently, and its execution order is not guranteed, so the output may appear in a different order each time.



Best use cases for thread and Runnable : 
- use extends Thread - if your class does not extend any other class
- Use implements Runnable - if your class already extends another class (preferred because java doesn't support multiple inheritance).


# Advantages of multithreading
- Improved performance - multiple tasks can run simultanously , reducing execution time.
- Efficient CPU utilization - Threads keep the CPU busy by running tasks in parallel time.
- Responsiveness - application (lke GUIs) remain responsive while performing background tasks.
- Resource sharing - threads within the same process share memory and resources, avoiding duplication.
- Better User experience - smooth execution of tasks like file downloads , animations , and real time updates.