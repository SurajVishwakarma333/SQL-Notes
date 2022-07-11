# SQL-Notes

### Define = SQL ?
   
- ***Structured Query Language (SQL)*** is a query language that allows us to perform operations on a database, such as creating entries, reading content, updating     content, and deleting entries.Basically CRUD operations.
- **SQL** is supported by almost any database you will likely use.

### Define = Database ?
   
- A **database** is an application that stores a collection of data.

### Define = Relational DataBase Management System (RDBMS) ?
 
- **RDBMS** database deals the data in the form of tables.
  
### Primary Key 

- A **primary key** is unique. A key value can not occur twice in one table. With a key, you can only find one row.

### Foreign Key 

- A **foreign key** is the linking pin between two tables.

_______________________________________________________________________________________________________________________________________________________________________
 
 
# CRUD(Create, Read, Update, and Delete) Operations Concept :

### • Create Database :
The CREATE DATABASE statement is used for creating a new database. The syntax is −

      SQL> CREATE DATABASE DATABASE_NAME;

**Example**
The following SQL statement creates a Database named Employee :

      SQL> CREATE DATABASE Employee;


### • Drop Database
The DROP DATABASE statement is used for deleting an existing database. The syntax is −

      SQL> DROP DATABASE DATABASE_NAME;
      
**Example**
The following SQL statement drop/delete a Database named Employee :

      SQL> DROP DATABASE Employee;      
      
      
### • Create Table
The CREATE TABLE statement is used for creating a new table. The syntax is −

      SQL> CREATE TABLE table_name
           (
              column_name column_data_type,
              column_name column_data_type,
              column_name column_data_type
              ...
           );

**Example**
The following SQL statement creates a table named Employees with four columns −

      SQL> CREATE TABLE Employees
          (
            id INT NOT NULL ,
            age INT NOT NULL,
            name VARCHAR(255),
            surname VARCHAR(255),
            PRIMARY KEY ( id )
          );     

### • Drop Table
The DROP TABLE statement is used for deleting an existing table. The syntax is −

      SQL> DROP TABLE table_name;

**Example**
The following SQL statement deletes a table named Employees −

      SQL> DROP TABLE Employees;
      
      
      
### • INSERT Data
The syntax for INSERT, looks similar to the following, where column1, column2, and so on represents the new data to appear in the respective columns −

      SQL> INSERT INTO table_name VALUES (column1, column2, ...);

**Example**
The following SQL INSERT statement inserts a new row in the Employees database created earlier −

      SQL> INSERT INTO Employees(id,age,name,surname) VALUES (100, 18, 'Suraj', 'Vishwakarma');


**Insert Data Only in Specified Columns**

It is also possible to only insert data in specific columns.
The following SQL statement will insert a new record, but only insert data in the "name" only.

      SQL> INSERT INTO Employees(name) VALUES ('Swapnil')      




### • SELECT Data
The SELECT statement is used to retrieve data from a database. The syntax for SELECT is −

      SQL> SELECT column_name, column_name, ...
      FROM table_name
      WHERE conditions;
The WHERE clause can use the comparison operators such as =, !=, <, >, <=,and >=, as well as the BETWEEN and LIKE operators.

**Example**
The following SQL statement selects the age, first and last columns from the Employees table, where id column is 100 −

      SQL> SELECT age, name, surname 
           FROM Employees 
           WHERE id = 100;
The following SQL statement selects the age, first and last columns from the Employees table where first column contains Zara −

      SQL> SELECT name, surname, age 
           FROM Employees 
           WHERE first LIKE '%Suraj%'
           
           
           
### • UPDATE Data
The UPDATE statement is used to update data. The syntax for UPDATE is −

      SQL> UPDATE table_name
      SET column_name = value, column_name = value, ...
      WHERE conditions;

The WHERE clause can use the comparison operators such as =, !=, <, >, <=,and >=, as well as the BETWEEN and LIKE operators.

**Example**
The following SQL UPDATE statement changes the age column of the employee whose id is 100 −

      SQL> UPDATE Employees SET age=20 WHERE id=100;           



### • DELETE Data
The DELETE statement is used to delete data from tables. The syntax for DELETE is −

      SQL> DELETE FROM table_name WHERE conditions;
The WHERE clause can use the comparison operators such as =, !=, <, >, <=,and >=, as well as the BETWEEN and LIKE operators.

**Example**
The following SQL DELETE statement deletes the record of the employee whose id is 100 −

      SQL> DELETE FROM Employees WHERE id=100;
      
      
      
# Some Important topics to be covered while studying sql.

  Use this "Customers" table as an examples:
   
     Select * from Customers;

![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)


### 1 : Distinct = skip duplicate.

**• SELECT Example Without DISTINCT :**

      SELECT Country FROM Customers;
      
![1](https://user-images.githubusercontent.com/101108540/178257025-a27d0b42-2212-46fb-8ae3-de18f92bf839.jpg)
 
      
**• SELECT Example With DISTINCT :**   

        SELECT Distinct Country FROM Customers; 
        
![2](https://user-images.githubusercontent.com/101108540/178257051-7d41f9fa-0ada-4760-a8ff-fb3d54aa560f.jpg)
        
        
  Use this "Customers" table as an examples:
   
     Select * from Customers;

![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)
_______________________________________________________________________________________________________________________________________________________________________

### 2 : SQL WHERE Clause = The WHERE clause is used to filter records.

WHERE Clause Example 1:

         SELECT * FROM Customers
         WHERE Country='Mexico';
         
![11](https://user-images.githubusercontent.com/101108540/178260840-d0076493-56d0-488d-b41d-b6cebffa3499.jpg)
         

WHERE Clause Example 2:

         SELECT * FROM Customers
         WHERE CustomerID=1;
         
 ![2](https://user-images.githubusercontent.com/101108540/178260866-536a663e-12a8-462f-a7fc-d86697b98d4c.jpg)
     
