### Introduction to DBS - 2 (Chris Bryant)

_2020-09-28 15:00:00 - 2020-09-28 16:00:00_

#### Database Management Systems

DBMS are software systems which enabled users to control databases.

Example functions the DBS can be used for are:

* Controlling and protecting access to the database  
* Defining, creating and deleting databases  

A DMBS has four useful properties:

* Data integration (the efficient storing and de-duplication of data)  
* Data integrity (Ensuring data is not corrupted or incorrect)  
* Data security (Protects data against loss, deliberate damage or unauthorised access)  
* Data independence (Creates an abstraction on top of the actual physical data storage, provides logical models for accessing the data)

DBMS provide a language (SQL) which enables users to query the database without needing to be concerned about the underlying data storage.

DBMS improve productivity (because it provides built-in functions), improve maintenance (because the underlying storage is decoupled from its usage) and improved backup and recovery services (because of interoperability and standardisation and built-in backup and recovery features).

As a result of all these extra features and layers of abstraction, DBMS have the following drawbacks:

* They are complicated  
* The software is very large and takes up a lot of storage space  
* They can be expensive if you need licencing keys  
* The time cost of converting (transitioning) from an older database system to a DBMS is high  
* The performance of a general-purpose DBMS may not be as good as a custom database system written for a specific purpose  

#### Database environmnent roles

* Administrator (consults and advises managers, pushes forward corporate objectives)  
* Database designers  
* Application programmers (the people who create software which utilisies the database)  
* End users (People who ingest the database in their daily work)  

#### Relational Databases

Relational databases are the most common type of DBMS currently in use. Relational databases are based on a paper by E.F.Codd published in 1970.

In relational databases, data is stored in files called relations (in the industry these are called tables). A relation consists of rows and columns. Typically a relation carries data on one kind of entity (eg. Students, Bakeries, Dogs, etc).

Tables contain columns (AKA attributes) and rows (AKA tuples or records), juust like a normal spreadsheet. Tables require unique identifiers for each row (in case the table contains duplicate data) to differentiate between rows. These unique identifiers are normally stored in a column which contains a **PRIMARY KEY**. The primary key is normally the first column in the table.

Columns can be used to link together two different tables with a link (aka, the relationship in the relational database). A column which is linked to the primary key of another table is called a **FOREIGN KEY**.

#### further reading

Students should read Chapter 1 of Connolly, T. & Begg, C. (2014). Database Systems: A Practical Approach to Design,
Implementation and Management: Global Edition. Number ISBN: 9781292061184. Pearson, sixth edition.
