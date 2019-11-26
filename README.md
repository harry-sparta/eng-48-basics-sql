# SQL Basics Notes
## Docker
### What is Docker?
**Def.** Docker is open source and a tool designed to make it easier to create, deploy, and run applications by using containers. Docker is a bit like a virtual machine. But unlike a virtual machine, rather than creating a whole virtual operating system, Docker allows applications to use the same Linux kernel as the system that they're running on and only requires applications be shipped with things not already running on the host computer. This gives a significant performance boost and reduces the size of the application.

### What is a container?
**Def.** Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, thanks to the container, the developer can rest assured that the application will run on any other Linux machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code.

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
