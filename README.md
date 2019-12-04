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
- **SELECT** <column>
- * <all columns>
- **FROM** <table>
- **AS**
- **WHERE**
  - <column name condition 1> **AND** <column condition 2>..... etc
  - <column condition 1> **OR** <column condition 2>..... etc
  - <column name> **IN** (<value 1>, <value 2>…)
  - **WHERE** <column> **NOT IN** (<value 1>, <value 2>…)
  - **WHERE** <column> **BETWEEN** (< lesser value >, <greater value>…)
  - **LIKE** <%pattern%>
- Wild cards
  - **%** zero or more charcters <%pattern%>
    - *'bl%'* finds any thing with bl at the front
  - **_** represent any single character
    - *'h_t'*
  - **[]** represent any characters in the brackets
    - *'h[oat]'*
  - **^** represents any characters not in the brackets
    - *'h[^oa]'*
  - **-** represents a range of characters
    - *'a-b'
- **IS NULL**
- **IS NOT NULL**
- **ORDER BY** <column> **ASC**/**DESC**
- **TOP** <# of rows> <column>
- <table> **OFFSET** <skipped rows> **ROWS FETCH NEXT** <# of rows> **ROWS ONLY**
- **DISTINCT** <column>
- Aggregate functions:
  - **GROUP BY** <column with common value>
    - **HAVING** <alias> <operator> <value>
  - **SUM(**<numeric column>**)**
  - **AVG(**<numeric column>**)**
  - **MAX(**<numeric column>**)**
  - **MIN(**<numeric column>**)**
- **COUNT(**<column>**)**
- **ROUND(**<number>, <decimals>**)**
- **CREATE TABLE** <table> <column 1 datatype key, column 2 datatype key, .....>  
  - if creating a primary key *CREATE TABLE enrollment (id INT IDENTITY PRIMARY KEY)*
  - if creating a foreign key *CREATE TABLE enrollment (id INT IDENTITY PRIMARY KEY, course_id INT FOREIGN KEY REFERENCES course(id), spartan_id INT FOREIGN KEY REFERENCES employee(id))*
- **IDENTITY** <start> <increment>
  - This is an auto-increment feature used to auto generate unique records e.g. when creating primary key it generates an id for user automatically, id insert not required during *INSERT TABLE, VALUES()* step.
- **ALTER TABLE** <table>
  - **ADD** <column> <data type> <key>
  - **ALTER COLUMN** <column> <data type> <key>
  - **INSERT INTO** <table>
    - **VALUES** <column 1, column 2, etc.>
      - if selecting foreign key *VALUES ('Room 1', (SELECT academy.id FROM academy))*
- **UPDATE** <table>
  - **SET** <column 1> <condition>, <column 2> <condition>,....etc
  - **WHERE** <condition> for rows
    - if no *WHERE* condition set, all rows will be updated
- String functions
  - **UPPER(**<value or column>**)**
  - **LOWER(**<value or column>**)**
  - **SUBSTR(**<value or column>, <start>**,** <length>**)**
  - **REPLACE(**<original value or column>**,** <target string>**,** <replacement string>**)**
  - **CONCAT(**<string 1>, <string 2>, ....etc **)**
  - **CHARINDEX(**<substring>, <string>, <start>)
    - returns the position of <substring> in <string> and 0 if no result
  - **FORMAT(**<value>, <format>)
    - e.g. turning 1000000 to 1,000,000.00 *FORMAT(UnitPrice,'#,##0.##')*
- Date functions
  - **GETDATE()** returns current date and time of Database
  - **DATEDIFF(**<interval>, <date 1>, <date 2>**)**
    - differences between 2 dates, <intervals> can be:
      - year, yyyy, yy = Year
      - quarter, qq, q = Quarter
      - month, mm, m = month
      - dayofyear = Day of the year
      - day, dy, y = Day
      - week, ww, wk = Week
      - weekday, dw, w = Weekday
      - hour, hh = hour
      - minute, mi, n = Minute
      - second, ss, s = Second
      - millisecond, ms = Millisecond
  - **DATEADD(**<interval>, <numeber>, <date>**)**
    - returns the new date with the interval added
  - **DATEFORMAT(**)
- Joins (brackets for full join name)
    - **(INNER) JOIN**
    - **LEFT (OUTER) JOIN**
    - **RIGHT (OUTER) JOIN**
    - **FULL (OUTER) JOIN**
- **CASE**
