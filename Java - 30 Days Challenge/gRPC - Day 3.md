## What is gRPC?
- Created by Google and it's an open-source Remote Procedure Call (RPC) protocol meant to enable flawless communication across dispersed systems.
- RPC frameworks enables simple and effective communication between services.
- gRPC = Google Remote Procedure Call.
- gRPC have speed advantages, it employs protocol buffers for serialization and HTTP/2 as it transport protocol instead of RESTful APIs using JSON over HTTP/1.1
- it allows one application to call a method running on another application as if it were a local method.
- instead of Application A directly accessing Application B's database, it can call : User user = userService.getUser(101); the request is sent over the network using gRPC.
  

## How gRPC Works?

Client -> gRPC -> HTTP/2 Connection -> Server -> Business Logic

	## gRPC Commonly uses : 
	- HTTP/2 for network transport
	- Protocol Buffers for message/data format
	- TLS for secure communication
	- Unary / streaming RPCs for communication patterns

## Where gRPC is used?
- grpc is particularly used in microservice architectures.
- instead of every service communicating through REST/JSON, internal services can communicate through gRPC.

## Why gRPC is so much popular?

1. **Performance** - mostly because of HTTP/2 and protocol buffers, multiple requests and responses transmitted over a single TCP connection.
2. **Language Support** - gRPC is great for language support which allows developers to select appropriate language for their service and still be able to interact with services created in other language.
3. **Streaming** - gRPC offers four kinds of streaming option in between both the sides.

## Architecture of gRPC 
The architecture of gRPC centers on Protocol Buffers' definiton of service methods and messages.
- Protocol Buffers let developers specify gRPC services and their approaches in .proto files. these files list the RPC techniques with remote calling capability together with the types of requests and responses.
- From these, gRPC instruments create client code and server code .proto files in many languages, offering the required stubs and skeletons to run the services.

## Features of gRPC
1. Cross-Language Support - given gRPC's support of several languages, polyglot settings would be perfect, promoting flexibility and creativity.
2. Load Balancing - Built-in client-side load balancing features of gRPC enaable distribution of incoming requests among several server instances, this gurantees that system may manage heavy traffic loads without affecting performance, therefore enhancing the scability and availability of the services.
3. Pluggable Authentication - gRPC offers custom authentication systems, OAuth for authorization, SSL/TLS for encrypted communication. this gurantees safe connection between services,therefore safrguarding private information and stopping illegal access.

## Conclusion 
for creating scalable, interoperable, and efficient distributed systems, Protocol Buffers and gRPC used together provide a potent mix. while gRPC offers a high-performance, versatile framework for remote procedure calls, Protocol buffers guarantee that messages are serialised in a compact, language-agnostic form. Microservices architectures, where dependable and effective communication is absolutely vital, call for this mix especially.

---
