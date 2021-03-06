# SQL-Notes

### Define = SQL ?
   
- ***Structured Query Language (SQL)*** is a query language that allows us to perform operations on a database, such as creating entries, reading content, updating     content, and deleting entries.Basically CRUD operations.
- **SQL** is supported by almost any database you will likely use.

### Define = Database ?
   
- A **database** is an application that stores a collection of data.

### Define = Relational DataBase Management System (RDBMS) ?
 
- **RDBMS** database deals the data in the form of tables.
  
### Primary Key 

- A **primary key** is unique identifier for each records in the table. A key value can not occur twice in one table.

- We cannot store **NULL** value in the primary key.

- We cannot change/delete the primary key values.

### Unique Key 

- A **Unique key** is also a unique identifier for records when the primary key is not present  in the table.

- We can store **Null** value in unique key,but only one value is allowed.

- We can modify the uique key values.

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
      
_______________________________________________________________________________________________________________________________________________________________________ 
![Screenshot 2022-07-19 122424](https://user-images.githubusercontent.com/101108540/180154594-bfb0b718-ee2f-48fd-9d10-71235d4de167.jpg)
     
 _______________________________________________________________________________________________________________________________________________________________________     

 ![Screenshot 2022-07-19 122342](https://user-images.githubusercontent.com/101108540/180142579-e1388552-c237-4299-a7f1-ce4eafb3fd19.jpg)
     
_______________________________________________________________________________________________________________________________________________________________________      
# Some Important topics to be covered while studying sql.

★  Use this "Customers" table as an examples:
   
     Select * from Customers;

![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)


### 1 : SQL Distinct = skip duplicate.

**• SELECT Example Without DISTINCT :**

      SELECT Country FROM Customers;
      
![1](https://user-images.githubusercontent.com/101108540/178257025-a27d0b42-2212-46fb-8ae3-de18f92bf839.jpg)
 
      
**• SELECT Example With DISTINCT :**   

        SELECT Distinct Country FROM Customers; 
        
![2](https://user-images.githubusercontent.com/101108540/178257051-7d41f9fa-0ada-4760-a8ff-fb3d54aa560f.jpg)
        
_______________________________________________________________________________________________________________________________________________________________________
        
 ★ Use this "Customers" table as an examples:
   
     Select * from Customers;

![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)

### 2 : SQL WHERE Clause = The WHERE clause is used to filter records.

**• WHERE Clause Example 1:**

         SELECT * FROM Customers
         WHERE Country='Mexico';
         
![11](https://user-images.githubusercontent.com/101108540/178260840-d0076493-56d0-488d-b41d-b6cebffa3499.jpg)
         

**• WHERE Clause Example 2:**

         SELECT * FROM Customers
         WHERE CustomerID=1;
         
 ![2](https://user-images.githubusercontent.com/101108540/178260866-536a663e-12a8-462f-a7fc-d86697b98d4c.jpg)
     

![3](https://user-images.githubusercontent.com/101108540/178262073-c423f86c-65ef-4278-8212-e977d6f12481.jpg)

_______________________________________________________________________________________________________________________________________________________________________
        
★  Use this "Customers" table as an examples:
   
     Select * from Customers;
     
![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)     

### 3 : SQL AND, OR and NOT Operators 

**• AND Example**

         SELECT * FROM Customers
         WHERE Country='Germany' AND City='Berlin';
         
 ![1](https://user-images.githubusercontent.com/101108540/178264335-44fda380-1511-4722-b844-4e001c6f006f.jpg)
             
         
**• OR Example**

         SELECT * FROM Customers
         WHERE City='Berlin' OR City='München';
         
 ![2](https://user-images.githubusercontent.com/101108540/178264380-aa6b4fcc-ca50-4430-9b93-4b6c1ba057bc.jpg)
        
         
**• NOT Example**

         SELECT * FROM Customers
         WHERE NOT Country='Germany';         
         
![3](https://user-images.githubusercontent.com/101108540/178264409-b447b3f9-016b-44f2-8ef3-b7bc10826b99.jpg)

_______________________________________________________________________________________________________________________________________________________________________
        
★  Use this "Customers" table as an examples:
   
     Select * from Customers;
     
![exm](https://user-images.githubusercontent.com/101108540/178256575-979830c5-72d8-48d2-a63a-a15e5790d9b3.jpg)


### 4 : SQL ORDER BY Keyword = used to sort the result-set in ascending or descending order.

**• ORDER BY Example**

         SELECT * FROM Customers
         ORDER BY Country;          //by default it will take as ascending order
         
![1](https://user-images.githubusercontent.com/101108540/178271119-dfcbd3c1-6f11-4175-a0fa-66386ff2556f.jpg)
             
**• ORDER BY DESC Example**

         SELECT * FROM Customers
         ORDER BY Country DESC;
         
![2](https://user-images.githubusercontent.com/101108540/178271140-95abea3c-d88e-4723-a82c-b1c875dc2a19.jpg)

_______________________________________________________________________________________________________________________________________________________________________
        
★  Use this "Products" table as an examples:
   
     Select * from Products;
     
![product](https://user-images.githubusercontent.com/101108540/178272714-9647bf5c-b0c3-4c30-bb0f-b587fc1add68.jpg)
     
  
### 5 : SQL MIN() and MAX() Functions  

**• MIN() Example = The MIN() function returns the smallest value of the selected column.**

         SELECT MIN(Price) FROM Products;
         
 ![1](https://user-images.githubusercontent.com/101108540/178275157-a757fe49-d2b6-492d-a951-fdbc6e0af68b.jpg)
        

**• MIN() Example = The MAX() function returns the largest value of the selected column.**

         SELECT MAX(Price) FROM Products;
         
![2](https://user-images.githubusercontent.com/101108540/178275185-2c559ab3-7e18-441c-a1bb-6b0fd3efd82d.jpg)

_______________________________________________________________________________________________________________________________________________________________________
        
★  Use this "Products" table as an examples:
   
     Select * from Products;
     
![product](https://user-images.githubusercontent.com/101108540/178272714-9647bf5c-b0c3-4c30-bb0f-b587fc1add68.jpg)

### 6 : SQL COUNT(), AVG() and SUM() Functions

**• COUNT() Example = The COUNT() function returns the number of Records.**

         SELECT COUNT(ProductID)
         FROM Products;
         
 ![1](https://user-images.githubusercontent.com/101108540/178495610-a8bafaf5-1058-4fc3-84bb-c96b958c03b7.jpg)     

**• AVG() Example = The AVG() function returns the average value of a numeric column.**

         SELECT AVG(Price)
         FROM Products;
         
  ![2](https://user-images.githubusercontent.com/101108540/178496342-e478c49e-b955-4996-988c-ce3c18bad9e9.jpg)
                

**• SUM() Example = The SUM() function returns the total sum of a numeric column.**

         SELECT SUM(Price)
         FROM Products;
         
![3](https://user-images.githubusercontent.com/101108540/178496663-845d51fe-93ba-4c32-a707-92b272c41c9b.jpg)
  
_______________________________________________________________________________________________________________________________________________________________________
  
★  Use this "Products" table as an examples:
   
     Select * from Products;
     
![product](https://user-images.githubusercontent.com/101108540/178272714-9647bf5c-b0c3-4c30-bb0f-b587fc1add68.jpg)       

### 7 : SQL LIKE Operator

**• LIKE Example = The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.**


         SELECT * FROM Products
         WHERE ProductsName LIKE 'a%';

![1](https://user-images.githubusercontent.com/101108540/178499036-9de21c4f-c549-42ae-a09e-809d75b3d04b.jpg)

![Screenshot 2022-07-12 185040](https://user-images.githubusercontent.com/101108540/178499909-ec14aed9-725b-4eb1-afe9-6cf9124cbcdc.jpg)

_______________________________________________________________________________________________________________________________________________________________________
  
★  Use this "Products" table as an examples:
   
     Select * from Products;
     
![product](https://user-images.githubusercontent.com/101108540/178272714-9647bf5c-b0c3-4c30-bb0f-b587fc1add68.jpg)       

### 8 : SQL BETWEEN Operator

**• BETWEEN Example = The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.**

         SELECT * FROM Products
         WHERE Price BETWEEN 10 AND 20;
         
![1](https://user-images.githubusercontent.com/101108540/178501657-8fdac6c0-ff99-46f4-9e86-8feb1857cebd.jpg)
    
**• NOT BETWEEN Example = The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.**

         SELECT * FROM Products
         WHERE Price NOT BETWEEN 10 AND 20;
         
![2](https://user-images.githubusercontent.com/101108540/178501985-427fe93e-a9d9-47c9-bdb6-0e33a44106b2.jpg)

_______________________________________________________________________________________________________________________________________________________________________

### 9 : SQL Aliases  

![1](https://user-images.githubusercontent.com/101108540/178723724-4a550f16-4919-466c-a2f1-ba2e0f3868f1.jpg)
_______________________________________________________________________________________________________________________________________________________________________

### 10 : SQL JOIN         

A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

![111111](https://user-images.githubusercontent.com/101108540/180604277-b14e22de-d809-4ce8-b7ac-73a7a6e77528.jpg)


**I. INNER JOIN = returns rows when there is a match in both tables.**
            
**II. LEFT JOIN = returns all rows from the left table,even if there are no matches in the right table.**

**III. RIGHT JOIN = returns rows when there is a match in one of the tables.**

**IV. Full JOIN = returns rows when there is a match in one of the tables.**

**V. SELF JOIN = is used to join a table to itself as if the table were two tables,temporarily renaming atleast one table in the SQL statement.**

**VI. CROSS JOIN = produces a result set which is the number of rows in the first table multipied by the number of rows in the secod tables. This kind of result is called as Cartesian Product.**


### 11 : SQL ORDER BY Keyword 

The ORDER BY keyword is used to sort the result-set in ascending or descending order.

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

![0](https://user-images.githubusercontent.com/101108540/180167411-c68316fa-4dc8-4381-8a7f-79b4c3452daa.jpg)

![1](https://user-images.githubusercontent.com/101108540/180167433-37efefff-537e-476c-8b4f-22a81ce81d67.jpg)

![2](https://user-images.githubusercontent.com/101108540/180167449-cd25adda-69fa-49dc-8188-95bb5f4ace4f.jpg)

![4](https://user-images.githubusercontent.com/101108540/180167892-12b21a02-b798-4aba-bdfa-20871d4c94b3.jpg)


### 12 : STORED PROCEDURE

- A stored procedure is also called as database object., because it get stored in database permanently.
- A stored procedure can be stored in the database and can be reused over and over again.
- We can pass parameter in stored procedure .,because we can do programming in stored procedure.

**Types of stored procedure :**

1. **User defined stored procedure :** User defined stored procedure are created by developer/user.

2. **System defined stored procedure :** System defined stored procedure are pre define function which was already present in sql server.


**Example :**

         Select * from employee;
       
![a](https://user-images.githubusercontent.com/101108540/180221997-40f1bb85-97e5-45a2-ba93-a22654d81b32.jpg)
 
       
_______________________________________________________________________________________________________________________________________________________________________

![demmm](https://user-images.githubusercontent.com/101108540/180218944-91461ca2-7f3c-4f75-a2f1-2c0056027c05.jpg)

once Stored procedure created if we want to update or do something then instead of CREATE we have to write AlTER thats it.


**TYPES OF PARAMETER IN STORED PROCEDURE :**

**1.Input Parameter :**

![1111](https://user-images.githubusercontent.com/101108540/180422932-63d98582-db03-4d71-b228-36c8ecf15f7f.jpg)


**2.Output Parameter :**

![2 ](https://user-images.githubusercontent.com/101108540/180441418-d2f935bb-4003-44bc-81ae-d036a4a9c245.jpg)
