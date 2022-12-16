[Back](/README.md/)

In MySQL, an aggregate function is a function that performs a calculation on a set of values and returns a single value. Some common aggregate functions in MySQL are SUM, AVG, MIN, and MAX. These functions are often used in conjunction with the GROUP BY clause to calculate statistics for each group of rows.

Here is an example of a SELECT statement with an aggregate function (AVG) and a GROUP BY clause that returns the average salary for each department:



`SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;` 

You can also use multiple aggregate functions in the same query. For example, the following SELECT statement returns the minimum, maximum, and average salary for each department:



`SELECT department, MIN(salary) AS min_salary, MAX(salary) AS max_salary, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;` 

It is important to note that the GROUP BY clause is used to group the rows of the result set into subsets based on the values in one or more columns. The aggregate functions are then applied to each group of rows.
