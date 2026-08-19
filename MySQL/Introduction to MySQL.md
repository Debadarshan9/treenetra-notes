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

# Date: 17-August-2026

### **What is constraint ?**

&rarr; Constraints are the rules applied to table columns to control the type of data stored in that column.

**1. NOT NULL**

&rarr; It ensures that a column must have a value.

&rarr; It can't contain `null`.

**2. UNIQUE**

&rarr; It ensures that duplicate values are not allowed in a column.

**3. PRIMARY KEY**

&rarr; A constraint that uniquely identifies that each record in a table.

&rarr; It can't contain `null` or `duplicate value`.

**4. FOREIGN KEY**

&rarr; A constraint used to create a relation between 2 tables.

&rarr; It references a primary key in another table.

**5. CHECK**

&rarr; It ensures that the value entered satisfies a specified condition.

**6. DEFAULT**

&rarr; It automatically provies a default value when no value is supplied during insertion.

| PRIAMRY KEY                                | UNIQUE                                        | FOREIGN KEY                           |
| ------------------------------------------ | --------------------------------------------- | ------------------------------------- |
| Uniquely identifies each record in a table | Ensures values in a column are not duplicated | Creates relationship between 2 tables |
| Identifies a row                           | Prevents duplicate data                       | Maintains relationship between tables |
| Duplicate values are not allowed           | Duplicate values are not allowed              | Duplicate values are allowed          |
| Null values are not allowed                | Null Values are allowed                       | Null values are allowed               |
| Only one per table                         | Multiple per table                            | Multiple per table                    |

```SQL
create table emp(
    emp_id int primary key,
    emp_name varchar(30) not null,
    email varchar(40) unique ,
    age int check (age >= 18),
    city varchar(50) default "BBSR"
);

insert into emp values(1,"Debadarshan","deba@hebbale.ai",24,default);

insert into emp values(2,"Ekita",null,23,default);
```

# Date: 18-August-2026

### **Aggregate Function**

An aggregate function performs a calculation for multiple rows and returns one result.

**1. COUNT()**

It returns the number of rows in a column

**Types**

count(column_name) &rarr; It will not count `null` values.

count(\*) &rarr; It will count `all` (includes null) values.

count(distinct_column_name) &rarr; Provides `unique` value.

**2. SUM()**

It returns the total values in a column, It ignores null value.

**3. AVG()**

It returns the average of numeric values, it ignores null value.

**4. MAX()**

It returns the highest value from a column(string,numeric,date), it ignores null value.

**5. MIN()**

It returns the lowest value from a column(string,numeric,date), it ignores null value.

```sql
create table test_emp(
emp_id int primary key,
emp_name varchar(30),
department varchar(20),
salary int,
bonous int
);

insert into test_emp values
(101,"Dibya","Testing",40000,5000),
(102,"Rahul","Testing",50000,6000),
(103,"Anita","Development",60000,7000),
(104,"Suman","Development",50000,null),
(105,"Priya","Testing",null,4000);

select * from test_emp;

-- Find the total number of employees
select count(*) from test_emp;

-- Count employees who have a salary
select count(salary) from test_emp;

-- Find the number of different department
select count(distinct department) from test_emp;

-- Find the total salary of all employee
select sum(salary) from test_emp;

-- Find the total bonous
select sum(bonous) from test_emp;

-- Find the average salary
select avg(salary) from test_emp;

-- Find the highest salary
select max(salary) from test_emp;

-- Find the lowest salary
select min(salary) from test_emp;
```

# Date: 19-August-2026

### **What is caluse ?**

A clause is a part of sql statement that tells the databse what data we want and how we want to filter, group, sort or limit it.

**1. SELECT**

It sprecifies which columns or data we want to retrive.

**2. FROM**

It specifies which table we want to retreive data from.

**3. WHERE**

It filters individual rows based on a condition.

**4. ORDER BY**

It sorts the result in ascending(asc) o descending(desc) order.

**5. GROUP BY**

It groups rows having the same value, usually for aggregate calculations.

**6. DISTINCT**

It removes the duplicate values from the result.

**7. HAVING**

It filters groups after group by clause.

**8. JOIN**

It combines data from two or more tables based on a related column.

**9. LIMIT**

It restricts the no. of rows return.

**10. OFFSET**

It tells sql how many rows to skip before returing the result.

| WHERE                                             | HAVING                         |
| ------------------------------------------------- | ------------------------------ |
| Filters individual rows                           | Filters groups                 |
| It applied before grouping                        | It applied after grouping      |
| It can't directly filter with aggregate functions | It can use aggregate functions |

```sql
create table department(
dept_id int primary key,
dept_name varchar(30),
location varchar(20),
employee int,
budget int
);

insert into department values
(1,"Testing","BBSR",25,500000),
(2,"Development","HYD",40,800000),
(3,"HR","BBSR",10,300000),
(4,"Testing","HYD",30,500000),
(5,"Development","Pune",35,700000),
(6,"Support","Delhi",15,400000);

select * from department;

select dept_name, location from department;

-- Department having more that 20 employees
select dept_name from department where employee > 20;

-- Department in desc order of employees
select * from department order by dept_name asc;

-- Unique department name
select distinct dept_name from department;

-- Find the no. of department in each location
select location, count(*) as dept_count
from department
group by location;

-- Find locations having more than 1 department
select location, count(*) as count_dept
from department
group by location
having count_dept > 1;

-- Find the departments where the location is BBSR
select dept_name
from department
where location = "BBSR";

-- Display only the first 3 departments
select * from department limit 3 offset 3;
```
