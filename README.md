
# MySQL Notes


SQL is a eclarative langauage 
MySQL is relational database that describe data and the relationship between data entities

A database is used for organize/manipulate data and for persistent data


#### Normalization


### Basic Query

##### SELECT Clause

Retrieve row/s from table 

~~~~
SELECT type, maker FROM cars;
~~~~

~~~~
SELECT <column name>, <colume name> FROM <table name>;
~~~~

Will return a two columns
~~~~
SELECT 'hello', 'github'
~~~~


> SELECT * FROM <table_name>
> Bad query because selecting everything from the table and increase disk I/O
> Best practices is to be specific and define in the query. 

##### FROM Clause

Specifying the table or constrain the query result

~~~~
SELECT type, maker FROM cars;
~~~~

##### INSERT Clause

Add row/s into tables

~~~~
INSERT INTO cars (maker, color)
VALUE('Tesla', 'black');
~~~~

##### UPDATE Clause

Modify row/s in table

~~~~
UPDATE cars SET maker = 'Honda' WHERE id = 1;
~~~~

##### DELETE Clause

Remove row/s from table

~~~~
DELETE FROM cars contacts where id = 2;
~~~~

> Using alias to distinguish column and their association with table. Important when using join query
> ~~~~ 
> SELECT c.maker, c.color, b.maker FROM cars c, bicycle b;
> ~~~~
>
> Commenting in MySQL workbench with '--'
> ~~~~
> -- SELECT ........ FROM ........
> ~~~~


##### Distinct qualifier 
Remove duplicate, only display uniques data

~~~~ 
SELECT DISTINCT c.maker, c.color FROM cars c;
~~~~


##### WHERE CLAUSE
Constrains the the query result set; can use boolean expression
> (<, >, =, <=, >=,)

~~~~
SELECT c.owner
FROM car c
WHERE c.maker = 'Tesla';
~~~~

Combining boolean expression (AND, OR)
~~~~
SELECT c.owner
FROM car c
WHERE c.maker = 'Tesla' 
AND c.licenseplate = 'ABCDE';
~~~~

> Other operator include BETWEEN, LIKE, IN, IS, IS NOT 


##### ORDER BY

~~~~
SELECT c.owner, c.maker
FROM car c
ORDER BY c.owner;
~~~~


##### Set Function 
Compute new value from column 
(COUNT, MAX, MIN, AVG, SUM)

~~~~
SELECT SUM(c.milage)
FROM car c
WHERE c.owner = 'Bill';
~~~~

> Execution Order
> FROM -> WHERE -> GROUP BY -> HAVING -> SELECT -> DISTINT -> ORDER BY


##### GROUP BY Clause
Break output set into subsets 
Run set function against each subset 

~~~~
SELECT COUNT(c.owner)
FROM car c
GROUP BY c.maker;
~~~~


##### HAVING Clause
Works like WHERE clause to restrict result 

~~~~
SELECT DISTINT(c.owner)
FROM car c
HAVING SUM(c.milage) < 5000;
~~~~




### Joining Tables

> The JOIN clause allow merges multiple tables into one result set


<p align="center">
  <img src="https://i.stack.imgur.com/UI25E.jpg">
  <br/>
</p>

##### CROSS JOIN clause

> Simplest JOIN, least useful 
> All rows from both tables 

~~~~
SELECT c.maker, o.owner
FROM cars c, owner o;


~~~~


##### INNER JOIN 


##### OUTER JOIN 

##### LEFT OUTER JOIN 


##### RIGHT OUTER JOIN 


##### SELF JOIN 

