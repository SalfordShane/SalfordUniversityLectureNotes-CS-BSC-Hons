### First tutorial (Maher Turifi)

_2020-09-30 10:00:00 - 2020-09-30 10:50:00_

Students were asked to download Microsoft Access to their computers and then download the worksheets and database files from Blackboard.

#### Structured Query Language

SQL is an acronym for `Structured Query Language`. It is a language designed to query relational databases in a (reasonably) human readable format which abstracts away the need to think about the underlying data structure of the database.

In the booklet students were prompted to open a database, navigate to the "Query Builder" menu and then execute some simple SQL queries in the following format:

```
SELECT * FROM Customer;
```

Where the above query translates to the following:

```
SELECT                     *                      FROM                      Customer;
{Give me this}             {* means everything}   {Give it me from: }       {The Customer table in the database}

```

You will note above that all SQL queries end with a semi-colon (one of these ;). This tells the SQL server that the query has ended - this is useful because you can send multiple queries in a single "request" to the server. 

Students were then asked to expand on these queries by adding `WHERE` clauses to their queries:

```
SELECT * FROM Customers WHERE Country = "Brazil";
```

The `WHERE` clause is used to filter the data you receive. The above query will, in plain English, `give me everything from the customers database table where the customer's country column is equal to the word "Brazil"`.

#### Case sensitivity

SQL queries are case in-sensitive. This means that it doesn't matter if you write `FROM`, `from` or `FrOm`. The names of tables and columns (in the above query, `Customers` and `Country`) can also be written in any case.

The only data which is case insensitive is the string (the word) "Brazil" because you are comparing values stored in a row in the database. Logically, "Brazil" does not equal "brazil", because the first has an upper-case B and the second has a lower case "b". This distinction is important to learn.
