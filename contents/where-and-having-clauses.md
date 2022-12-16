[Back](/README.md/)

In MySQL, the WHERE clause is used to filter rows from a SELECT, UPDATE, or DELETE statement based on certain conditions. The WHERE clause is used in the following syntax:



`SELECT column1, column2, ...
FROM table_name
WHERE condition;` 

The condition in the WHERE clause can be any expression that evaluates to a boolean value (true or false). If the condition evaluates to true, the row will be included in the result set; if it evaluates to false, the row will be excluded.

Here is an example of a SELECT statement with a WHERE clause that returns all employees with a salary greater than $50,000:



`SELECT name, salary
FROM employees
WHERE salary > 50000;` 

The HAVING clause is similar to the WHERE clause, but it is used to filter groups of rows rather than individual rows. The HAVING clause is used in the following syntax:



`SELECT column1, column2, ...
FROM table_name
GROUP BY column1, column2, ...
HAVING condition;` 

The condition in the HAVING clause is applied to the groups of rows after they have been grouped by the GROUP BY clause. If the condition evaluates to true, the group of rows will be included in the result set; if it evaluates to false, the group of rows will be excluded.

Here is an example of a SELECT statement with a GROUP BY and HAVING clause that returns the average salary for each department, but only for departments with an average salary greater than $60,000:



`SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;` 
