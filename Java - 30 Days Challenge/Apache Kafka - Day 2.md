Apache Kafka is a distributed event streaming platform used to send,receive,store, and process large amounts of data in real time.

Kafka acts as a high-performance middle layer that allows different applications/services to communicate with each other through streams of events or messages.


  ![[Pasted image 20261006075312.png|338]]

## What is the need of Kafka?
- Kafka is mainly used when an application needs to handle large volumes of events/data reliably and in real time.

## Important Kafka Concepts
1. **Producer** - producer sends messages/events to Kafka.
		Application -> Producer -> Kafka
		producer.send("OrderCreated");

2.  **Consumer** - Consumer reads messages from Kafka.
		Kafka -> Consumer -> Application

3. **Topic** - A topic is a logical category where Kafka stores events.
		for ex: orders, payments, users, notifications

4. **Partition** - A topic can be divided into multiple partitions.
		                   ![[Pasted image 20261006080132.png|130]]
	Partition allow Kafka to process large amounts of data in parallel.

5. **Broker** - A Kafka broker is a Kafka server. A Kafka cluster can contain multiple brokers.
6. **Consumer Group** - Multiple consumers can work together as a consumer group.
		             ![[Pasted image 20261006080545.png]]
	this allows processing to be distributed across multiple application instances.


## Advantages of Kafka
1. High Throughput
2. Scalability
3. Fault tolerance
4. Durability
5. Real-time processing
6. Loose Coupling
7. Message replay

## Disadvantages of Kafka
1. Complexity
2. Operational head
3. Not ideal for simple applications
4. Resource Consumption

## Where is Kafka Used?
1. Microservices 
			![[Pasted image 20261006081248.png|203]]
2. Log aggregation
			![[Pasted image 20261006081320.png|136]]
3. IoT
			![[Pasted image 20261006081344.png|148]]
4. Financial Systems
			![[Pasted image 20261006081417.png|170]]

## Kafka in a Java/Sprong Boot Application
- Kafka is especially relevant for backend jobs.![[Pasted image 20261006081658.png|388]]
---
On day 3 we will do the implementation part of the Kafka to our java Spring Boot Project...till then if you have any query and suggestion for me reach me out at suraj.adi@outlook.com