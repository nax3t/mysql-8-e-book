[Back](/README.md/)

In MySQL, a stored procedure is a reusable program that can be stored in the database and called from within a MySQL application or from the command line. Stored procedures are often used to encapsulate complex logic, improve performance, and increase code reuse.

To create a stored procedure in MySQL, you can use the CREATE PROCEDURE statement in the following syntax:



`CREATE PROCEDURE procedure_name (parameter1 datatype, parameter2 datatype, ...)
BEGIN
  -- procedure body
END;` 

Here is an example of a stored procedure that calculates the total salary for a department:



`CREATE PROCEDURE total_salary (IN dept_id INT)
BEGIN
  SELECT SUM(salary) AS total_salary
  FROM employees
  WHERE department_id = dept_id;
END;` 

To call a stored procedure in MySQL, you can use the CALL statement in the following syntax:



`CALL procedure_name(parameter1_value, parameter2_value, ...);` 

For example, to call the 'total_salary' stored procedure with a department id of 1, you can use the following CALL statement:



`CALL total_salary(1);` 

In MySQL, a trigger is a database object that is automatically executed in response to certain events, such as an INSERT, UPDATE, or DELETE statement on a table. Triggers are often used to enforce data integrity, implement complex business logic, and maintain summary tables.

To create a trigger in MySQL, you can use the CREATE TRIGGER statement in the following syntax:



`CREATE TRIGGER trigger_name
AFTER/BEFORE INSERT/UPDATE/DELETE
ON table_name
FOR EACH ROW
BEGIN
  -- trigger body
END;` 

Here is an example of a trigger that updates the 'last_update' column of the 'employees' table every time a row is updated:



`CREATE TRIGGER update_last_update
AFTER UPDATE
ON employees
FOR EACH ROW
BEGIN
  SET NEW.last_update = NOW();
END;` 
