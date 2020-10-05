### Queries in Relational Databases (Chris Bryant)

_2020-10-05 13:00:00 - 2020-10-05 13:50:00_

#### Terminology

* Relation (table or file)  
* Tuple (row or record)  
* Attribute (column or field)  

Primary keys uniquely identify each row in a table (each tuple of a relation).

An attribute (or column) that is linked to the primary key in another table is known as a foreign key.

#### SQL (Structured query language)

A query is a question you ask the server about the data you want.

##### Select statements

The basid syntax of a `SELECT` query is:

```
SELECT <list of columns>
FROM <table name>
[ WHERE <condition(s)> ]
```

_The square brackets in the above query indicate that the WHERE part of the query is optional and doesn't need to be included._

For example:

```
SELECT id, username, password
FROM users
WHERE email = "test@example.com"
```

#### Drivers and penalty points

Dr Bryant gave a number of query examples which revolved around bad (car) drivers.

Here is the example table:

| driverID  | name  | address  | points  |
|---|---|---|---|
| d010  | Fred  | Perth  | 7  |
| d020  | Jimmy  | Dundee  | 4  |
| d030  | David  | Dundee  | 2  |
| d040 | John | Stirling | 3 |
| d050 | Bobby | Aberdeen | 12 |

##### Select example 1

List all the ids from the Drivers table:

```
SELECT driverID
FROM Drivers;
```

_Note: there is no sue of the WHERE clause here._

Results:

| driverID |
|---|
| D010 |
| D020 |
| D030 |
| D040 |
| D050 |

##### Select example 2

List all the ids (driverID) and points from the Drivers table:

```
SELECT driverID, points
DROM Drivers;
```

Results:

| driverID | points |
|---|---|
| D010 | 7 |
| D020 | 4 |
| D030 | 2 |
| D040 | 3 |
| D050 | 12 |

##### Select example 3

List all the attributes from the Drivers table:

```
SELECT * 
FROM Drivers;
```

Results:

The entire table will be output.

_Note: the asterix (*) means ALL COLUMNS (all attributes)._

##### Select example 4

List all the ids (driverID) of the drivers in the Drivers table who are from Dundee:

```
SELECT driverID
FROM Drivers
WHERE address = "Dundee";
```

Results:

| driverID |
|---|
| D020 |
| D030 |

These two rows are returned because both of these rows have the value `Dundee` in the `address` column.

##### The LIKE clause

In SQL, we can use the `=` syntax to perform an exact match. Using `=` we are asking: Do the first thing EXACTLY equal the second thing?

There is also a `LIKE` clause which can be used with prefixes, postfixes, wildcards, etc.

For example:

```
SELECT name, address
FROM Drivers
WHERE address LIKE "Du*"
```

This will return all the driver's names and addresses where the driver's address begins with the characters "Du".

Results:

| name | address |
|---|---|
| Jimmy | Dundee |
| David | Dundee |

##### The IN clause

In SQL, `IN` and `NOT IN` can be used to match columns against groups of values, for instance:

List all the drivers where their address is either Perth or Stirling:

```
SELECT name, address
FROM Drivers
WHERE address IN ('Perth', 'Stirling');
```

Returns:

| name | address |
|---|---|
| Fred | Perth |
| John | Stirling |

We can also INVERT the `IN` clauses using `NOT IN`, which matches columns against anything which is NOT in the groups of values, for instance:

```
SELECT name, address
FROM Drivers
WHERE address NOT IN ('Perth', 'Stirling');
```

Returns:

| name | address |
|---|---|
| Jimmy | Dundee |
| David | Dundee |
| Bobby | Aberdeen |

###### Less than and more than

Select all the drivers who's license points are between 7 and 15:

```
SELECT name, points
FROM Drivers
WHERE points >= 7 AND points <= 15;
```

You will notice in the above query that the less-than, more-than, less-than-or-equals and more-than-or-equals clauses use the normal mathematical notation.

This results in:

| name | points |
|---|---|
| Fred | 7 |
| Bobby | 12 |

#### Editor's note an an apology

I found Dr Bryant to be moving through the lecture information too quickly. At this point I stopped taking notes. My goal with these notes is to compress the information given and make it more friendly to the students and I'm concerned about throwing hundreds of lines of information at you.

I don't think you're actually expected to know how JOINs, INNER-JOINs and OUTER-JOINs work by the end of this lecture so I've ommited it in the name of not creating a document so long that people won't actually read it.

When we cover JOINs properly in future lectures on their own I will cover them in my lecture notes.
