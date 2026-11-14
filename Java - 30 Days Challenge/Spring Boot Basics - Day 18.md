Java - Programming Language
Spring Framework - Framework for building java applications
Spring Boot - Makes spring application development easier
Spring MVC - Handles HTTP requests and responses
Spring Data JPA - Simplifies database operations
Hibernate - ORM implementation
MySQL - Stores application data
Maven - Manages dependencies and buils

---
Spring Boot is a java framework that helps developers build standalone , production-ready applications quickly with minimal configuration.

Imagine building a Student Management system
- Register Students
- Store Student information
- Retrieve student records
- delete student recrods
- connect your application to a database

in Spring Boot :
Contoller Layer (@RestController) - handles HTTP
Service Layer (@Service) - handles business logic
Repository Layer (@Repository) - Spring Data JPA
Database (MySQL / PostgreSQL) - Stores information


---
Dependency Injection - most important concepts in Spring Boot interviews

---
In spring boot projects - what each folder does 
src/main/java - your java source code
resources - configuration and static resources
application.properties - application configuration
src/test/java - test cases
pom.xml - maven dependencies and configuration
static - static files like css, js and images 
templates - server-side HTML templates

What is REST API ?
react application needs student information from java backend. the frontend sends an HTTP request to spring boot, spring boot processes it and returns a response.

React Frontend ------GET /Hello ----- Spring Boot Backend ----Returns Response ---"Hello, welcome to spring boot".

@RestController - it tells spring that this class handles REST API requests and returns response data directly.
@GetMapping ("/hello") - it maps HTTP GET requests to the /hello URL to this method.

---
HTTP methods - 
GET - retrieve data
POST - create data
PUT - Update data
DELETE - delete data