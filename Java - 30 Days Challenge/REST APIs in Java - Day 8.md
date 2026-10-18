
First understand what is API (application programming interface)?
imagine you are using a food delivery application
1. you place an order - you select food and click the order button in the app.
2. the API receives your request - the backend checks the order, processes it, and communicates with the database.
3. the API returns a response - the app receives information such as the order ID, order status, and total price.

an API (application programming interface) allows two software applications to communicate with each other through a defined interface.

for ex :
- Frontend : React or React Native
- Backend : java with spring boot
- Database : MySQL or PostgreSQL
frontend sends a request to the backend API. the backend processes it and returns a response.

###### What is REST API?
REST stands for representational State Transfer. it is an ***architectural style for designing network*** APIs.
a REST APIs commonly uses HTTP to let a client create,retreive,update and delete resources.

For EX:
GET /api/products
GET /api/products/10
POST /api/products
PUT /api/products/10
PATCH /api/products/10 - update only some portion not whole
DELETE /api/products/10

these endpoints represent operations on products.

API is the general concept of an interface between software.
REST is an architectural style for designing APIs.
HTTP is the protocol commonly used to send REST APIs requests.
spring boot is a java framework that makes implementing these APIs easier.

Let's say frontend requests a list of products
1. the client sends GET /api/products.
2. spring boot routes the request to a java controller
3. the controller calls a service to execute the business logic
4. the service retreives products through a repository
5. the repository communicates the results into JSON
6. the client receives an HTTP response.

client and server communicates over network ; they don't need to use the same programming language.

###### Every API request can contain 4 main parts
1. URL - where the request is sent.
   http://localhost:8080/api/products/10
2. HTTP method - what opertion you want to perform.
   GET
3. Headers - extra information about the request
   Accept : application/json
   Authorization : Bearer your-token
4. Body - data sent to the server , usually POST or PUT
   {
	   "name" :  "Laptop",
	   "price" : 55000
   }

A request doesn't always need every part. for ex. a simple GET request often has no body and authentication headers are only needed when the endpoint requires them.

###### What is JSON?
JSON stands for javascript Object Notation. lightweight format for exchanging data between applications.

EX: 
{
	"id" : 10
	"name" : "Laptop"
	"price" : 55000
	"available" : true
}

the equivalent java object for this JSON could look like this :
public class product {
	private Long id;
	private String name;
	private double price;
	private boolean available;
	
	// Getters and Setters
}

spring boot commonly uses the ==🔴jackson library== to convert java objects to JSON and JSON to java objects.
this conversion is called :
- Serialization : Java object -> JSON
- Deserialization : JSON -> Java Object

###### HTTP Methods
1. GET - used to retrieve the data
2. POST - used to create a resource
3. PUT - used to replace/ update a resource
4. PATCH - used to partially update a resource
5. DELETE - used to delete a resource

###### Difference between PUT and PATCH
suppose a product has this data
{
"name" : "Laptop"
"price" : 55000
"brand" : "Dell"
}
you want to change only the price.
So for this PATCH, might suited because it will only send
{
"price" : 50000
}

with PUT , the usual convention is to send the complete replacement representation:
{
"name" : "Laptop"
"price" : 50000
"brand" : "Dell"
}
exact behavior depends on your API contract. PUT is defined as replacement-oriented, while PATCH applies partial modifications.

###### Safe and Idempotent
- safe : the method is intended not to change server state. GET is safe.
- Idempotent : repeating the same request has the same intended effect as making it once.
  
GET,PUT,and DELETE are generally idempotent. ==🟢POST is not inherently idempotent==.
PATCH may or may not be idempotent depending on how it is designed.

###### HTTP status codes
a status code tells the client what happened to its request.
2xx - sucess
4xx - client-side request errors
5xx - server side errors

###### REST API Interview questions
1. What is REST API?
   an api designed around REST architectural constraints, commonly exposing resources over HTTP.
2. what is the difference between REST and HTTP?
   REST is an architectural style; HTTP is a communication protocol commonly used to implement REST APIs.
3. Diff between PUT and Patch?
   PUT is replacement-oriented and PATCH applies partial modifications.
   
   
   ---
That's it for today for any queries mail me at hisurajshah@outlook.com