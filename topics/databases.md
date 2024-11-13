# Databases and SQL

## Overview

Understanding databases is crucial for managing and analyzing data. This section covers relational database concepts, SQL commands, and database management.

## Key Concepts

- **Relational Database Management**: Understanding tables, primary keys, and foreign keys.
- **SQL Commands**: `SELECT`, `FROM`, `WHERE`, `JOIN`, `ORDER BY`, `GROUP BY`, `INSERT`, `UPDATE`, `DELETE`, `CREATE TABLE`, `ALTER TABLE`.

## Databases in the Study Design

### Unit 3 Outcome 1

**Key Knowledge:**

- structural characteristics of relational database management systems (RDBMS), including:
  - data types and field sizes
  - data in tables
  - relationships using primary and foreign key fields
  - use of SQL to generate queries
- techniques for identifying, selecting, extracting and validating authentic data stored in large repositories, including:
  - downloading datasets in a range of formats
  - the use of SQL functions to retrieve, filter, sort and link dataset values (SELECT, FROM, WHERE, ORDER BY, INNER JOIN)
  - the use of Boolean operators (AND, NOT, OR) for WHERE statements
  - existence checking, type checking and range checking
- techniques for testing databases and spreadsheets, including:
  - testing formula and query results
  - testing validation
  - test cases comparing expected and actual results in testing tables

**Key Skills:**

- identify, select, extract and validate relevant data from large repositories using database software

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028.*
**© Victorian Curriculum and Assessment Authority. For current versions and related content visit [www.vcaa.vic.edu.au](https://www.vcaa.vic.edu.au)**

---

### Unit 4 Outcome 1 Note

*While databases may be used in the Unit 4 Outcome 1 SAT task, the key knowledge and key skills do not directly mention database use.*

---

## Learning Resources

- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- [SQL Commands Cheat Sheet](https://www.sqltutorial.org/sql-cheat-sheet/)

## Relational Database Management

### What is a database?

A database is an organized collection of data, typically stored and accessed electronically from a computer system. **Relational Databases** are databases that model the data in tables with rows and columns. Each **table** represents an entity, and each **row** represents a record. The **columns** represent attributes or fields. In relational databases, tables are linked using foreign key to primary key relationships.

### Primary Key and Foreign Key Relationships

A **primary key** is a unique identifier for each record in a table. It must contain unique values and cannot be NULL. A **foreign key** is a field in a table that links to the primary key in another table. This establishes a relationship between those two tables.

For example, in an `employees` table, the `employee_id` could be the primary key. In a `departments` table, the `department_id` could be the primary key. If each employee belongs to a department, the `department_id` in the `employees` table would be a foreign key linking to the `department_id` in the `departments` table.

This means that we can retrieve all the information about each employees department (location, department name, phone number, manager, etc.) without needing to rewrite that information for each employee in the department. This is an important feature of relational databases.

## Examples

### Example 1: Basic SQL Queries

#### Select all columns from students where their age is equal to 17

```sql
SELECT * FROM students WHERE age = 17;
```

#### Select the name and age columns from students and order them by age in descending order

```sql
SELECT name, age FROM students ORDER BY age DESC;
```

#### Insert a new student into the students table

```sql
INSERT INTO students (first_name, last_name, age, year_level) VALUES ('John', 'Doe', 17, 11);
```

#### Update a specific student's year level

```sql
UPDATE students SET year_level = 12 WHERE student_id = 131;
```

### Example 2: Creating a Database Table

```sql
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name VARCHAR(100),
    age INTEGER
);
```
