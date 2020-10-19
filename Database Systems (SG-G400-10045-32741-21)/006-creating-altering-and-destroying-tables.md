### Creating, Altering and Destroying tables (Chris Bryant)

_2020-10-19 13:00:00 - 2020-10-19 13:50:00_

As well as using SQL to query to select, update and delete data in a database table, we can also use queries to modify and create databases.

#### Nullable data

The value `NULL` indicates that the value is unknown, for example you could use it for an `address` table where you don't know a customer's address yet.

`NULL` is a special data type and is not the same as `0` or `false`.

#### Creating a table

The basic syntax for creating a table is:

```sql
CREATE TABLE <table name> (
    <column name> <data type> [<default value>] [<column constraints>],
    <column name> <data type> [<default value>] [<column constraints>],
    ...
    ...
    [<table contstraint>]
);
```

For instance, to create a table with the following columns: `studentID, title, name, address` you could use the following SQL:

```sql
CREATE TABLE students (
    studentID INTEGER,
    title VARCHAR(4),
    name VARCHAR(20),
    address VARCHAR(20)
);
```

#### Constraints

Column constraints as seen in the syntax query above can be used to restrict the data which can be entered in to a table.

##### NOT NULL

`NOT NULL` can be used to force a column to have a value which is not `NULL`. For instance:

```sql
CREATE TABLE students (
    studentID INTEGER,
    title VARCHAR(4),
    name VARCHAR(20) NOT NULL,
    address VARCHAR(20)
);
```

The above query will generate the same table but will enforce the constraint that `name` must not be `NULL`.

##### Declaring a primary key

`PRIMARY KEY` constraints are used to uniquely identify a row in a table. When a column has a primary key, it is telling the DBMS that that column will always be unique, `NOT NULL` and can be used to permanently identify a single row.

For example:

```sql
CREATE TABLE students (
    studentID INTEGER PRIMARY KEY,
    title VARCHAR(4),
    name VARCHAR(20) NOT NULL,
    address VARCHAR(20)
);
```

In the query above you do not need to declare `studentID` as `NOT NULL` as this is the default for a `PRIMARY KEY` column. **A table can only have column which is a primary key.**

##### Foreign keys

Foreign keys are used to make a column reference a column in another table - it's used to link together two tables to make querying between them easier.

Suppose that we had another table called `courses` and we wanted to reference the `courses` table in a `course` column in the student table, we could write:

```sql
CREATE TABLE students (
    studentID INTEGER PRIMARY KEY,
    title VARCHAR(4),
    name VARCHAR(20) NOT NULL,
    address VARCHAR(20),
    course INTEGER REFERENCES courses(courseID)
);
```
