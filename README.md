# SQL-Review
SQL Guide &amp; Example


Part 1 – Introduction to SQL Queries

 SQLQuery Definition:
SQL (StructuredQuery Language): A domain-specific language used to manage and manipulate relational databases. SQL allows users to perform tasks such as retrieving, inserting, updating, and deleting data from a database.

 SQL SELECT Statement:
SELECT Statement: An SQL statement used to retrieve data from one or more database tables.
  
Query Example:
SQL
SELECT * FROM Employees;


 Part 2 – Single Table SQL Queries

 SQL SELECT Clause:
SELECT Clause: A SQL clause used to specify the columns you want to retrieve from a table.
  
 SQL WHERE Clause:
WHERE Clause: A SQL clause used to filter rows based on a specified condition.

Query Example:
SQL
SELECT FirstName, LastName FROM Employees WHERE Department = 'HR';


 Part 3 – Multi-table Queries

 SQL JOIN Clause:
-JOIN Clause: A SQL clause used to combine rows from two or more tables based on a related column.

 SQL INNER JOIN:
-INNER JOIN: A type of SQL join that combines rows from two or more tables based on a related column between them, only returning rows where there is a match in both tables.

Query Example:
SQL
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
INNER JOIN Orders
ON Customers.CustomerID = Orders.CustomerID;


 SQL OUTER JOIN:
-OUTER JOIN: A type of SQL join that returns all rows when there is a match in one of the tables, and NULL values where there is no match.

Query Example:
SQL
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT OUTER JOIN Orders
ON Customers.CustomerID = Orders.CustomerID;


 Part 4 – SQL Subqueries

 SQL Subquery:
-Subquery: A query embedded within another query. Subqueries are often used to retrieve data to be used in the main query's condition.

Query Example:
SQL
SELECT ProductName
FROM Products
WHERE SupplierID IN (SELECT SupplierID FROM Suppliers WHERE Country = 'USA');


 Part 5 – SQL Set Operators

 SQL UNION Operator:
UNION Operator: A SQL set operator used to combine the result sets of two or more SELECT statements into a single result set.

Query Example:
SQL
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2017
UNION
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2018;


 SQL INTERSECT Operator:
INTERSECT Operator: A SQL set operator used to retrieve the common rows between two result sets.

Query Example:
SQL
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2017
INTERSECT
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2018;


 SQL EXCEPT Operator:
EXCEPT Operator: A SQL set operator used to retrieve rows from the first result set that are not present in the second result set.

Query Example:
SQL
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2017
EXCEPT
SELECT SKU, SKU_Description, Department
FROM CATALOG_SKU_2018;


Query Order
Field > Tables > Joins, Subqueries > Functions, Group by
