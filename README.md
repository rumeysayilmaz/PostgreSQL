## Fundamentals of Database Systems: An Introduction

__Database__ is a shared collection of logically related data and a description of this data, designed to meet the information needs of an organization [1].

Database is a single, large repository of data that may be used simultaneously by many deparments and users in an organization. It is not owned by a single department but is a shared corporate resource. Instead of having disconnected files with reduandant data, all the data items are integrated with a minimum amount of duplication [1].

Logically related data comprises of: entities, attributes and relationships of an organization’s information.

This data is extracted by analyzing the information needs of an organization. 

__Database Management System (DBMS)__: A software system that enables users to define, create, maintain, and control access to the database.

A DBMS allows users to define the database through a data definition language (DDL) that lets them specify the data types and structures and contraints on the data to be stored in the database. In addition to this, the users can insert, update, delete and retrieve data from the database through data manipulation language (DML). Furthermore, facilities such as security system, integrity system, concurrency control system, recovery control system with a user accessible catalog are provided [1].

### Components of a Database Management System Environment 
*Hardware* : Can range from a PC to a network of computers.

*Software* : DBMS, operating system, network software (if necessary) and also the application programs.

*Data* : Used by the organization and a description of this data called the schema.

*Procedures* : Instructions and rules that should be applied to the design and use of the database and DBMS.

*People*

## PostgreSQL
- Object relational database management system
- uses SQL as query language

PostgreSQL can be managed through various tools such as psql, pgAdmin, phpPgAdmin etc. 

psql is basically a command line based front-end to manage PostgreSQL. pgAdmin is a GUI based administration tool for PostgreSQL. phpPgAdmin is a web-based administration tool for PostgreSQL written in PHP.  
>[dbeaver](https://dbeaver.io/) is another multi-platform database tool that enables creation of Entity Relation diagrams 

[1] _Source: Connolly, T.M., & Begg, C. (2005). Database Systems: A Practical Approach to Design, Implementation, and Management (4th Edition). USA: Addison Wesley._
