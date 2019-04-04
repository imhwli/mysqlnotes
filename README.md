#MySQL Notes


####SQL's purpose 
1.Organize data
2.Persisten data
3.Manipulate data

Relational Database
Way to describe data and the relationship between data entities




####Normalization




####SELECT Clause
Retrieve row/s from table 

~~~~
SELECT type, maker FROM cars;
~~~~

####FROM Clause
Specifying the table 


####INSERT Clause
Add row/s into tables

~~~~
INSERT INTO cars (maker, color)
VALUE('Tesla', 'black');
~~~~

####UPDATE Clause
Modify row/s in table

~~~~
UPDATE cars SET maker = 'Honda' WHERE id = 1;
~~~~

####DELETE Clause
Remove row/s from table

~~~~
DELETE FROM cars contacts where id = 2;
~~~~