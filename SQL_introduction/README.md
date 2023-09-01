- # A directory for several tasks on SQL and database management
## Database:
A database is a structured collection of data that is organized in a way that allows for efficient storage, retrieval, and management of information. It is used to store various types data, such as a text, numbers, images, and more.
- Examples: MySQL, PostgreSQL, Oracle Database, Microsoft SQL server,etc.

## Relational Database
A relational Database is a type of database that organizes data into tables, where each table represents a specific entity or concept, and the relationships between these tables are defined by keys. 
- Examples: MySQL, PostgreSQL.

## SQL
SQL stands for Structured Query Languages. It'sa domain-specific language used to manage and manipulate relational databases.

## MySQL
MyQL is an open-source relational database management system. It's one of the most popular databases and is widely used for various applications, from web development to data analysis.

## How to create a DB in MYSQL
You use the `CREATE DATABASE` statement.
- Example: `CREATE DATABASE mydatabase;`
- Example 2: Specifyong Character Set and collation
    ``CREATE DATABASE employees
        CHARACTER SET utf8mb4
        COLLATE utf8mb4_unicode_ci;``

- Example 3

## DDL and DML
- DDL stands for Data Definition Language. It includes SQL statements used to define and manage the structure of the database, such as creating tables altering tables, and dropping tables.
- DML stands for Data Manipulation Language. It includes SQL statements used to manipulate data stored in the database, such as inserting, altering and deleing data.

## How to create or alter a table
Use the `CREATE TABLE` statement
- Example: `CREATE TABLE students (id INT, name VARCHAR(255))`

## How to SELECT data from a table
use the `SELECT` statement.
- Example: `SELECT name, age FROM students WHERE age > 20;`

## How to INSERT, UPDATE, OR DELETE table
Use the `INSERT INTO`, `UPDATE` and `DELETE FROM` to insert, update and delete respectively.
- Examples:
    - Insert: `INSERT INTO students (name, age) VALUES ('Alice', 25);`
    - Update: `UPDATE students SET age = 26 WHERE name = 'Alice';`
    - Delete: `DELETE FROM students WHERE age < 18;`
## Subqueries
Subqueries, also known as nested queries, are queries embedded within other queries. They allow you to retrieve data based on the results of another query.
- Example: `SELECT name FROM students WHERE age > (SELECT AVG(age) FROM students);`
## How to use MySQL Functions:
MySQL provides a variety of built-in functions for tasks like mathematical calculations, strings manipulation, data operations and more.
- Examples: `SELECT AVG(age) FROM students;`

## Setting up Virtual Machine on Ubuntu
### Ubuntu
- Open the Terminal application:
Now you will execute command line in your Terminal (each of them start with $)
- Install VirtualBox:` $ sudo apt-get install virtualbox`
- Install Vagrant: `$ sudo apt-get install vagrant`
- Add the Ubuntu 20.04 (Focal) image to your box list:` $ vagrant box add ubuntu/focal64` Warning: this step can take time
Many other images are available here
- Create your first virtual machine:
`$ vagrant init ubuntu/focal64` -> it will generate a Vagrantfile with base = "ubuntu/focal64" - you don’t have to execute this command line everyday, only once, to create a new virtual machine
- `$ vagrant up` -> it will start your virtual machine
- `$ vagrant ssh` -> now you are inside your virtual machine.