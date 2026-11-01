MySQL is a very popular open-source relational database management system (RDBMS).
- MySQL is open-source
- MySQL is free
- MySQL is ideal for both small and large applications
- MySQL is very fast, reliable, scalable, and easy to use
- MySQL is cross-platform
- MySQL is compliant with the ANSI SQL standard

### Who Uses MySQL
- Huge websites like Facebook, Twitter, Airbnb, Booking.com, Uber, Github, Youtube, etc.
- Content management systems like wordpress, drupal, Joomla, contao, etc
- A very large number of web developers around the world.

### Show Data on your web site
To build a website that shows data from a database, you will need:
- An RDBMS database program (like MySQL)
- A server-side scripting language, like PHP
- To use SQL to get the data you want
- To use HTML/CSS to style the page

### What is RDBMS
stands for relational database management system
program used to maintain a relational database
RDBMS is the basis for all modern database systems

### What is SQL?
SQL is the standard language for dealing with relational databases
SQL is used to insert, search, update, and delete records.

### Most important SQL commands
- SELECT - extracts data from a database
- UPDATE - updates data in a database
- DELETE - deletes data from a database
- INSERT INTO - inserts new data into a database
- CREATE DATABASE - creates a new database
- ALTER DATABASE - modifies a database
- CREATE  TABLE - creates a new table
- ALTER TABLE - modifies a table
- DROP TABLE - deletes a table
- CREATE INDEX - creates an index (search key)
- DROP INDEX - deletes an index

### MySQL SELECT DISTINCT statement
SELECT DISTINCT statement is used to return only distinct values.
in a table, a column may contain several duplicate values - and sometimes you want to list only the unique values.
SELECT DISTINCT country FROM Customers;

Count Distinct Values - by using the COUNT() function with the Distinct keyword, we can count the number of unique values.
SELECT COUNT(DISTINCT Country) FROM Customers;

### MySQL WHERE Clause
WHERE clause is used to filter records.
WHERE clause is used to extract only those records that fulfill a specific condition.

SELECT * FROM Customers
WHERE Country = 'Mexico';

*Following operators can be used in the WHERE clause:* 
- Equal =
- Greater Than >
- Less Than <
- Greater than or equal >=
- Less than or equal <=
- Not equal <> or !=
- BETWEEN - between a certain range
- LIKE - search for a pattern
- IN - to specify multiple possible values for a column

### MySQL ORDER BY Keyword
ORDER BY keyword is used to sort the result-set in ascending or descending order.
ORDER BY keyword sorts the records in ascending order (ASC) by default
To sort the records in descending order, use the DESC keyword.
SELECT * FROM Products
ORDER BY Price DESC;

### MySQL AND operator
WHERE clause can contain one or many AND operators
the AND operator is used to filter records based on more than one condition

SELECT * FROM Customers
WHERE Country = 'UK' AND City = 'London';

AND operator displays a record if all the condition are TRUE
OR operator displays a record if any of the condition are TRUE

### Combining AND and OR
we can also combine the AND and OR operators.

SELECT * FROM Customers
WHERE Country = 'Germany' AND (City = 'Berlin' OR City = 'Stuttgart');

### MySQL NOT Operator
NOT operator is used in the WHERE clause to return all records that DO NOT match the specified criteria. It reverses the result of a condition from true to false and vice-versa.

SELECT * FROM Customers
WHERE NOT Country = 'Germany';  Here NOT operator is used in combination with the = operator.

NOT operator is also used in combination with other operators to exclude data, such as
- NOT LIKE - used in the WHERE clause to exclude rows that match a specified character pattern.  A percent sign % represents zero, one, or multiple characters. A underscore sign _ represents a single character.
  SELECT * FROM Customers
  WHERE CustomerName NOT LIKE 'A%';
- NOT BETWEEN  - used in the WHERE clause to select rows where a value falls outside a specified inclusive range. NOT BETWEEN can be used with numeric, text or data values.
  SELECT * FROM Customers
  WHERE CustomerID NOT BETWEEN 10 AND 60;
- NOT IN - used in the WHERE clause to exclude rows that match any value in a specified list or a subquery result set.
  SELECT * FROM Customers
  WHERE City NOT IN ('paris' , 'London');
- IS NOT NULL
- NOT EXISTS

### MySQL INSERT INTO statement
INSERT INTO statement is used to insert new records in a table.

INSERT INTO Customers
VALUES ('cardinal', 'Tom B. Erichen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

IF insert data only in specific columns then
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');

### What is Null Value?
If a field in a table is optional, it is possible to insert or update a record without adding any value to this field. This way, the field will be saved with a NULL value.

A null value represents an unknown, missing, or inapplicable data in a database field. It is not a value itself, but a placeholder to indicate the absence of data.

To test for null values we can't test using =, < , or <>
we will have to use the IS NULL and IS NOT NULL operator instead.

SELECT column_name
FROM table_name
WHERE column_name IS NULL;

SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
![[Pasted image 20261101123600.png]]