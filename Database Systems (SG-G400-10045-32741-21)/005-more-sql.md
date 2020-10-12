### More SQL (Chris Bryant)

_2020-10-12 13:00:00 - 2020-10-12 13:50:00_

#### Attribute aliases

When writing a select query it can sometimes be useful to rename a column in the resulting data (or to have a shorter column name to use in the query). Imagine the following query:

```sql
SELECT driverID FROM Drivers;
```

Which returns:

| driverID |
|---|
| 1 |
| 2 |
| 3 |

We can easily change the attribute alias (the name of the column in the resulting query) using the `AS` keyword:

```sql
SELECT driverID AS driverNumber FROM Drivers;
```

Which returns the same data with a different column name:

| driverNumber |
|---|
| 1 |
| 2 |
| 3 |

#### DISTINCT keyword

The distinct keyword is used to deduplicate (remove duplicated rows) from the response of a SQL query:

Imagine the following query:

```sql
SELECT age, name FROM friends;
```

Which returns:

| age | name |
|---|---|
| 18 | David |
| 18 | Stephen |
| 19 | Patrick |

You can only get DISTINCT ages by running the following query:

```sql
SELECT DISTINCT age FROM friends;
```

| age |
|---|
| 18 |
| 19 |

You will notice that even though we have two friends aged 18, the age only shows once in the above query because of the DISTINCT keyword.

#### Group By

At this point in the lecture Dr Bryant began talking about GROUPBY and HAVING keywords. In all honesty this is a complex topic which these notes won't properly (and succinctly) express so I've provided some external resources you can read about these topics:

* [guru99 GROUP BY tutorial](https://www.guru99.com/group-by.html)  
* [Electric toolbox GROUP BY tutorial](https://electrictoolbox.com/mysql-group-by-having/)  

#### Changing data in tables

We are all familiar by this point with `SELECT` queries being used to GET data from a table. Another type of query is the `UPDATE` query which can be used to change data in a table.

UPDATE queries follow a different basic syntax to SELECT queries:

```sql
# An example SELECT query:
SELECT points FROM Drivers;

# An example UPDATE query:
UPDATE Drivers SET points = 6;
```

The update query above will change _every_ driver's license points to `6`. Obviously this isn't very useful and we probably only want to update a single driver:

```sql
UPDATE Drivers SET points = 6 WHERE driverID = 'D040';
```

The above query will do the following:

* Search the Drivers table
* Find a driver with the driverID `D040`
* UPDATE the points attribute (column) of the driver to `6`

#### Deleting rows in tables

`DELETE` is used to remove rows from a table:

```sql
DELETE FROM Drivers;
```

The above query will delete every row in the drivers table. Again, this isn't very useful and we should limit the deletions using a `WHERE` statement:

```sql
DELETE FROM Drivers WHERE driverID = 'D040';
```

The above query will do the following:

* Search the Drivers table
* Find a driver with the driverID `D040`
* DELETE that row from the table

DELETE is irrevocable. Once you run this query the data is gone forever (unless you have a backup mechanism in place).

#### Adding rows to tables

`INSERT` is used to add rows to a table. The syntax is more complicated than previous queryes we have seen as you need to define all the attributes (the data in each column):

`INSERT` queries have the following syntax format:

```sql
INSERT INTO <table name> (<column names>) VALUES (<column values>);
```

Like this:

```
INSERT INTO Drivers
(driverID, name, points)
VALUES
('D050', 'Md Ahmed', 6);
```

The paranthesis (round brackets) in the above query are **required**.
