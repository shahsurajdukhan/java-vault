Spring boot builds on the spring framework by eliminating boilerplate XML configurations and manual server deployments.

- Inversion of Control Container - core engine that creates,wires and manages object lifecycles. instead of your classes creating dependencies via new() , the container controls them.
- Dependency Injection - mechanism by which the IoC container injects required dependencies. constructor injection is preferred for immutability.
- Auto-Configuration - spring boot automatically configures your application based on the jar dependencies present on your classpath.
- Starter dependencies - curated dependency descriptors that bundle all required libraries together, eliminating version mismatch hell.
- Embedded Servers - ships with built-in servlet containers, meaning your app runs as a standalone executable JAR.


---
3-Tier layered architecture

1. Presentation/ Controller Layer - (@RestController) : entry point for incoming HTTP requests (GET, POST, PUT, DELETE). validates input, handles mapping, and converts java objects to JSON responses.
2. Bussiness / Service Layer (@service) - contains core business logic, transactional rules, data transformations (DTO to entity mappings), and workflow orchestration.
3. Persistence / Repository Layer (@Repository) - communicates directly with the database using spring data JPA interfaces to execute CRUD operations without writing raw boilerplate SQL.

---
@SpringBootApplication - meta annotation on the main class combining @configuration, @EnableAutoConfiguration, and @ComponentScan.

@RestController - marks a class as a web controller where return values are automatically written straight to the HTTP response body as JSON.

@RequestMapping / @GetMapping - maps HTTP requests to specific handler methods inside controllers.

@PathVariable / @RequestParam - extracts values from URL path segments ( /users/{id} ) vs. query parameters ( ?sort=asc )

@Service - stereotype annotations marking a class as belonging to the business/service layer.

@Repository - marks a persistence component and enables automatic JDBC/ORM exception translation.

@Autowired - injects object dependencies automatically via the Spring IoC container.

@Transactional - Ensures database operations execute atomically within a transaction boundary ( rolls back on runtime exceptions. )

@Entity & @Table - JPA markers declaring a standard POJO class as a relational database table mapping.
