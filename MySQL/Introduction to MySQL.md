# Date: 12-August-2026

### **What is DATA?**

Data means a collection of values of information that can be processed to get meaningfull information.

### **What is Database?**

A database is an organised collection of data that allows us to store, manage, retrive and update information efficiently.

**_Note: Instead of maintaning thousands of methods in notebooks we can store the data in database._**

### **What is DBMS?**

&rarr; DBMS is known as `Database Management System`.

&rarr; It is a software that allows us to get, store, manage, retrive, update and delete data from a database.

### **Database VS DBMS**

| Database           | DBMS                           |
| ------------------ | ------------------------------ |
| Collection of Data | Software that manages data     |
| It stores the data | It provides operations on data |
| Ex: select records | Ex: MySQL                      |

### **Types of DBMS**

### **1. Relational DBMS**

&rarr; Data is stored in tables consisting of `rows` and `columns`.

&rarr; Ex: MySQL, Oracle

### **2. Non-relational DBMS**

&rarr; It doesn't store the data in table format but it store the data as `documents` or `key-value pairs`.

&rarr; Ex: MonogoDB

### **What is SQL?**

&rarr; It is knowns as Structured Query Language.

&rarr; It is a language used to communicate in relational databases.

### **What is datatype**

&rarr; A datatype defines what kind of value a variable or databse column can store.

**1. Numeric Datatype**

&rarr; It is used to store numbers.

&rarr; `int`, `float`, `decimal`, `bool`

**2. String Datatype**

&rarr; It is used to store text or characters.

&rarr; `char`, `varchar`, `enum`, `set`

### **char vs varchar**

| char                         | varchar                         |
| ---------------------------- | ------------------------------- |
| Fixed length                 | Variable length                 |
| Always reserve define length | Uses space based on actual data |
| Best for fixed length values | Best for variable length values |
| Ex: pincode, county code     | Ex: Name, addresss, email       |

### **Date & time datatype**

&rarr; It is used to store data & time.

&rarr; `date`, `time`, `datetime`, `timestap`, `year`

# Date: 13-August-2026

### **DDL Command**

&rarr; It is known as Data Definition Language.

&rarr; It defines or changes the structure of database objects.

&rarr; `create`, `alter`, `drop`, `truncate` are some DDl commands.

### **Drop vs Truncate**

| DROP                                            | TRUNCATE                                                         |
| ----------------------------------------------- | ---------------------------------------------------------------- |
| It removes the entire table (structuare + data) | It removes all rows from the table but keeps the table structure |
| Table structure deleted                         | Table structure remains same                                     |
| It is slower than truncate                      | It is fast                                                       |

### **DML Command**

&rarr; It is known as Data Manipulation Language.

&rarr; It deals with the data of the table.

&rarr; It is used to insert, modify and delete data.

&rarr; `insert`, `delete`, `update` are some DML commands.

| Drop                           | Truncate                     | Delete                       |
| ------------------------------ | ---------------------------- | ---------------------------- |
| Drop is a DDL command          | Truncate is a DDL command    | Delete is DML command        |
| All data deleted               | All data deleted             | Specific data deleted        |
| It removes the table structure | It does not remove structure | Is does not remove structure |
| Where clause is not used       | Where caluse is not used     | Where clause is used used    |
| Rollback is not possible       | Rollback is not possible     | Rollback is possible         |

### **DCL Command**

&rarr; It is known as Data Control Language.

&rarr; It controls user access and permissions.

&rarr; `grant`, `revoke` are some DCL commands.

### **TCL Command**

&rarr; It is known as Transaction Control Language.

&rarr; It is used to manage the changes made by the DML commands.

&rarr; commit, rollback, savepoint,

**commit**

Permanetly save the changes made in the current transaction.

**rollback**

&rarr; It cancels the changes made in the current transaction since the last commit or transaction start.

&rarr; After commit rollback is not possible.

**savepoint:**

&rarr; It creates a checkpoint inside a transaction.

&rarr; We can rollback to that particular point without undoing the entire transaction.

```sql
create database AT26;
use AT26;

-- DDL Command (CREATE)
create table student(
    id int,
    name varchar(10),
    age int,
    course varchar(30)
);
desc student;
select * from student;

-- DML Command (INSERT)
insert into student values
(1,"Dibya",27,'Python'),
(2,"Rkesh",26,'SQL'),
(3,"Ajay",30,'AI');

-- DML Command (UPDATE)
set sql_safe_updates=0;
update student set course = 'Playwright' where id=2;

-- DML Command (DELETE)
delete from student where id=3;

-- DDL Command (ALTER)
alter table student add email varchar(10); -- add a col
alter table student drop column email; -- remove a col
alter table student rename column name to first_name; -- rename a col
alter table student modify first_name varchar(30);  -- modify data type

-- DDL Command (TRUNCATE)
truncate table student;
select * from student;

-- DDL Command (DROP)
drop table student;
```
