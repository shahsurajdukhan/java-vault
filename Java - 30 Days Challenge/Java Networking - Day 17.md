Java Networking refers to writing programs that execute across multiple devices(computers), in which the devices are all connected to each other using a network.

### Advantages of Java Networking
- Creating server-client applications
- Implementing networking protocols
- Implement socket programming
- Creating web services

The Java.net package for the J2SE APIs contains a collection of classes and interfaces that provide the low-level communication details, allowing you to write programs that focus on solving the problem at hand.

Java.net package provides support for the two common network protocols
- TCP - stands for transmission control protocol , which allows for reliable communication between two applications. TCP is typically used over the Internet Protocol , which is referrred to as TCP/IP.
- UDP - User Datagram Protocol, connection-less protocol that allows for packets of data to be transmitted between applications.

## Socket Programming in Java Networking
sockets provide the communication mechanism between two computers using TCP. A client program creates a socket on its end of the communication and attempts to connect that socket to a server.
When the connection is made, the server creates a socket object on its end of the communication. The client and the server can now communicate by writing to and reading from the socket.

The java.net.socket class represents a socket, and the java.net.ServerSocket class provides a mechanism for the server program to listen for clients and establish connections with them.

Following steps happens when establishing a TCP connection b/w two computers using sockets :
- Server instantiates a ServerSocket object, denoting which port number communication is to occur on.
- The server invokes the accept() method of the ServerSocket class. this method waits until a client connects to the server on the given port.
- After the server is waiting , a client instantiates a socket object, specifying the server name and the port number to connect to.
- The constructor of the socket class attempts to connect the client to the specified server and the port number. if communication is established, the client now has a socket object capable of communicatiing with the server.
- on the server side, the accept() method returns a reference to a new socket on the server that is connected to the client's socket.

After the connections are established , communication can occur using I/O streams. Each socket has both an OutputStream and an InputStream. the client's OutputStream is connected to the server's InputStream and the client's InputStream is connected to the server's OutputStream.

If the ServerSocket constructor does not throw an exception, it means that your application has successfully bound to the specified port and is ready for client requests.