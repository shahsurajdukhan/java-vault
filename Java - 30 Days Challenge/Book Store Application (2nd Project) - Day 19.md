## Things we need First
- Database (Repository) - Books : fetch all books (GET) & Order Books (POST)
- Service Layer - fetch all book , order book
- Controller - views, and templates which will be visible to the user.

Inversion of control. (IOC container)
dependency injection
Annotations - beans

**imp. annotations**
@async - email notification (service)
@profile - helps to switch different profiles
@Bean
@Configuration


---
Folder Structure of this project
SRC/
    --------main /
              ------------java/
                         ---------com/
                                 ---------bookstore/
                                             bookstoreapp.java
                                                       ---------------service/
                                                                   ----------books/ , order/