### Need of Thread Synchronization?
When we start two or more threads within a program, there may be a situation when multiple threads try to access the same resource and finally they can produce unforeseen result due to concurrency issues. For Example, if multiple threads try to write within a same file then they may corrupt the data because one of the threads can override data or while one thread is opening the same file at the same time another thread might be closing the same file.

So there is a need to synchronize the action of multiple threads and make sure that only one thread can access the resource at a given point in time. This is implemented using a concept called monitors. Each object in java is associated with a monitor, which a thread can lock or unlock. Only one thread at a time may hold a lock on a monitor.

### Thread Synchronization in Java
Java programming language provides a very handy way of creating threads and synchronizing their task by using synchronized blocks. You keep shared resources within their block. 

`synchronized(objectidentifier) {`
`// Access shared variables and other shared resources`
`}`
Here, the objectidentifier is a reference to an object whose lock associates with the monitor that the synchronized statement represents.

## JAVA - Block Synchronization
When we start two or more threads within a java program, there may be a situation when multiple threads try to access the same resource and finally they can produce unforeseen result due to concurrency issues.
so there is a need to synchronize the action of multiple threads and make sure that only one thread can access the resource at a given point in time. This is implemented using a concept called monitor.

## Static Synchronization 
When we use this type of synchronization then, if a thread is in the static synchronized region, all other threads trying to access this region will be blocked. since static methods belong to the class therefore, static synchronization applies class level lock.