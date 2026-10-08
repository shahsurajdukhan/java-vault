JPA stands for Java Persistence API

JPA is a Java Specification/API  used to store Java Objects in a relational database.
means JPA allows us to work with database table using Java objects instead of writing SQL for every operation.

for ex: without JPA, you might write SQL : SELECT * FROM users WHERE id  = 1;
	   with JPA, you can work with a Java object: User user = userRepository.findById(1L); JPA handles much of the database interaction for you.

## Diff between JPA and Hibernate
JPA - defines rules and interfaces for ORM.
Hibernate - this is an implementation of JPA

JPA tells us what should be done. Hibernate provides the actual implementation

JPA provides - @entity , @Id , @GeneratedValue
Hibernate understands these annotations and performs the actual database operations.

## What is ORM?
ORM stands for Object Relational Mapping
it maps java class to table of the database
        object into row
        and field into column

## Example of JPA 

`import jakarta.persistence.Entity;`
`import jakarta.persistence.Id;`

`@Entity`
`public class User {`

	`@Id`
	`private Long id;`
	`private String name;`
	`private String email;`
	
`}`


here important annotations are @Entity and @Id

what does @Entity mean - this java class should be mapped to a database table.
what does @Id mean - every entity needs a primary key.


## JPA Relationships
real applications don't have only one table.
JPA supports relationships such as :
@oneToone - One user has one profile. 
```
@OneToOne
private Profile profile;
```


@OneToMany - One user can have many orders.

```
@OneToMany
private List<Order> orders;
```

@ManyToOne - This is very common. Many orders belong to one user.

```
@ManyToOne
@JoinColumn(name = "user_id")
private User user;
```


@ManyToMany -  One student can take many courses. One course can have many students.
```
@ManyToMany
private List<Course> courses;
```

## In modern Spring Boot applications, we commonly use:
```
Spring Boot
     ↓
Spring Data JPA
     ↓
JPA
     ↓
Hibernate
     ↓
JDBC
     ↓
MySQL/PostgreSQL
```

## What is Hibernate doing?
- Hibernate performs the actual ORM work.
- Hibernate understands the mapping done by JPA.

## Conclusion

### JPA

**JPA (Java Persistence API)** is a **Java specification/API** that defines how Java objects can be mapped to and persisted in relational databases using **ORM (Object-Relational Mapping)**.

> **In simple words:** JPA defines the rules for connecting Java objects with database tables.

### Hibernate

**Hibernate** is an **ORM framework and a JPA implementation** that provides the actual functionality required to map Java objects to database tables and perform database operations.

> **In simple words:** Hibernate implements the rules defined by JPA and handles the actual interaction with the database.

### Easy way to remember

```
JPA       → What should be done? (Specification)
Hibernate → How it is actually done? (Implementation)
```

**Example:** JPA is like an **interface/contract**, while Hibernate is a **class that implements that contract**.


---
