# SQL Basics Notes
## Docker
### What is Docker?
**Def.** Docker is open source and a tool designed to make it easier to create, deploy, and run applications by using containers. Docker is a bit like a virtual machine. But unlike a virtual machine, rather than creating a whole virtual operating system, Docker allows applications to use the same Linux kernel as the system that they're running on and only requires applications be shipped with things not already running on the host computer. This gives a significant performance boost and reduces the size of the application.

### What is a container?
**Def.** Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, thanks to the container, the developer can rest assured that the application will run on any other Linux machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code.

### Connecting Docker
<PLACE HOLDER>

## SQL
### What is SQL?
**Def.** Structured query language

#### Types of language input
- Data manipulation language (DML)
  - SELECT
  - INSERT
  - UPDATE
  - DELETE
- Data definition language (DDL)
  - CREATE
  - ALTER
  - DROP
  - TRUNCATE
- Data control language (DCL)
  - GRANT
  - REVOKE
- Transaction control language (TCL)
  - COMMIT
  - ROLLBACK
  - SAVEPOINT

##### DML part is (80:20) of SQL
The DML part is also known as CRUD.
- Create
- Read
- Update
- Delete

##Database
### What is a Database
**Def.** <PLACE HOLDER>

### Types of Database
- Flat file Database
  - Stores everything in one table.
  - Good for small numbers of records related to a single topic.
- Relational Database
  - Gives you the ability to separate masses data into numerous tables.
  - They are linked to each other using keys (primary and foreign keys).
    - One to one
    - One to many
    - Many to many
- Big Data
  - MongoDB, Vertica etc.
  - Used for Data Analytics and Business Intelligence
  - Digital Age and Internet of Things

### Example Database tools
- Access (Microsoft)
  - Local database. Not too be used on external servers or build system on it.
- PostgreSQL
  - Popular because it is open source
- SQLite
  - Small database. Things goes into one file.
- MySQL
  - PHP based.
- Redis
  - Not only SQL based. Fast access to data.
- MongoDB
  - Not only SQL. It is an open source.
- ORACLE
  - Hold data for you. Can apply further ORACLE data services to the data held.

## SQL Cheat sheet
- SELECT <column name>
- * <all columns>
- FROM <table>
- AS
- WHERE
  - <column name condition 1> AND <column name condition 2>..... etc
  - <column name condition 1> OR <column name condition 2>..... etc
  - <column name> IN (<value 1>, <value 2>…)
  - WHERE <column name> NOT IN (<value 1>, <value 2>…)
  - WHERE <column name> BETWEEN (< lesser value >, <greater value>…)
  - LIKE <%pattern%>
