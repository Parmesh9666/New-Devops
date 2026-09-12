10/09/2026
What is index?
Index is a database data structure used to improve query performance and indexes consume storage and can slow down INSERT, UPDATE and DELETE operations.

What is Primary key and Foreign key?
Primary key is combination of UNIQ and NOT VALUES. It won't allow duplicates and null values into table.
Foreign Key is referential integrity. It refers to Primary key in another table.

Diff b/t Group By and Having?
Group by used to group the data and used with aggregate functions.
Having is used to filter the data after group by.

Diff b/t UNION and UNION ALL?
UNION combines result from two query's and removes duplicates.
UNION ALL will also perform the same and it will give all the data from two query's including duplicates and it is faster.

What is VIEW?
VIEW is a virtual table created one or more table using SQL query. It does not store data itself. It is used to simplify the complex query's and give result faster.

Ex:- Create VIEW emp_view AS
select emp_id, Emp_name from employee

What is sub query?
Sub query is nothing but there will be another query inside the query.

What is Join and how many types of joins are there?
Joins is used to combine both tables and gives out put and there different types of joins are there.
They are:
Inner join: It will give all matching records from the tables
Left join: It will give all records from the left table and matching records from the right table.
Right join: It will give all records from the right table and matching records from the left table.
Full join: It will give all records from both tables, including matching and non-matching records. For non-matching records, it returns NULL values.
Cross join: Each record from the first table joins with each record in second table. Ex., T1=3 and T2=4 total 3*4=12

