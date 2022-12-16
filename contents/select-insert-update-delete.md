In MySQL 8, the SELECT, INSERT, UPDATE, and DELETE statements are used to retrieve, add, modify, and delete data in a database. These statements are commonly referred to as "CRUD" (create, read, update, delete) operations.

Here is a brief overview of these statements:

* SELECT: The SELECT statement is used to retrieve data from a database. For example, the following statement retrieves all rows from the "employees" table:



`SELECT * FROM employees;` 

You can use various clauses and functions to filter, sort, and transform the data that is retrieved.

* INSERT: The INSERT statement is used to add new rows to a database table. For example, the following statement inserts a new row into the "employees" table:



`INSERT INTO employees (id, name, salary) VALUES (1, 'John Smith', 50000);` 

* UPDATE: The UPDATE statement is used to modify existing rows in a database table. For example, the following statement updates the salary of the employee with an ID of 1:



`UPDATE employees SET salary = 55000 WHERE id = 1;` 

* DELETE: The DELETE statement is used to delete rows from a database table. For example, the following statement deletes the employee with an ID of 1:



`DELETE FROM employees WHERE id = 1;` 

These are just a few examples of how you can use the SELECT, INSERT, UPDATE, and DELETE statements in MySQL 8. You can use these statements in combination with other SQL commands and clauses to perform a wide range of data manipulation tasks.