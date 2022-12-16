In MySQL, an index is a data structure that improves the speed of data retrieval operations on a database table. Indexes can be created on one or more columns of a table, and they allow the database server to find and retrieve the requested data much faster than it would be able to without an index.

There are several types of indexes in MySQL, including PRIMARY KEY, UNIQUE, and INDEX. The PRIMARY KEY index is used to uniquely identify each row in a table and cannot contain null values. The UNIQUE index is similar to the PRIMARY KEY index, but it allows null values and can be used on multiple columns. The INDEX index is used to improve the performance of SELECT, UPDATE, and DELETE statements and can be used on multiple columns.

To create an index on a table, you can use the CREATE INDEX statement in the following syntax:



`CREATE INDEX index_name
ON table_name (column1, column2, ...);` 

Here is an example of a CREATE INDEX statement that creates an INDEX index on the 'last\_name' and 'first\_name' columns of the 'employees' table:



`CREATE INDEX name_index
ON employees (last_name, first_name);` 

Performance optimization in MySQL involves identifying and addressing any bottlenecks that may be causing slow performance of your database. Some common performance optimization techniques include using indexes, optimizing queries, and using appropriate data types and storage engines.

Here are a few examples of performance optimization techniques in MySQL:

1.  Using indexes: As mentioned above, creating indexes on frequently used columns can significantly improve the performance of SELECT, UPDATE, and DELETE statements.
    
2.  Optimizing queries: You can optimize the performance of your queries by using appropriate WHERE clauses, avoiding unnecessary columns in the SELECT list, and using appropriate JOIN types.
    
3.  Using appropriate data types and storage engines: Choosing the right data types and storage engines for your tables can significantly improve the performance of your database. For example, using the InnoDB storage engine for tables with heavy read/write workloads and the MyISAM storage engine for tables with mostly read-only workloads can improve performance.
