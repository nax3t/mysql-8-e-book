[Back](/README.md/)

In MySQL, a subquery is a SELECT statement that is nested within another SELECT, UPDATE, INSERT, or DELETE statement, or within another subquery. Subqueries are often used to return data that will be used in the outer query as a condition for the WHERE or HAVING clause, or as a value for an INSERT, UPDATE, or DELETE statement.

Here is an example of a subquery that returns the names of all departments where the number of employees is greater than 5:



`SELECT department_name
FROM departments
WHERE (SELECT COUNT(*) FROM employees WHERE department_id = departments.id) > 5;` 

A join, on the other hand, is used to combine rows from two or more tables based on a related column between them. There are several types of joins in MySQL: INNER JOIN, OUTER JOIN (LEFT JOIN, RIGHT JOIN, FULL JOIN), CROSS JOIN, and NATURAL JOIN.

Here is an example of an INNER JOIN that returns the names and salaries of employees in the 'Sales' department:



`SELECT employees.name, employees.salary
FROM employees
INNER JOIN departments ON employees.department_id = departments.id
WHERE departments.department_name = 'Sales';` 