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

---
*Unit 4 Outcome 1 Note*

*While databases may be used in the Unit 4 Outcome 1 SAT task, the key knowledge and key skills do not directly mention database use.*

---

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028.*
**© Victorian Curriculum and Assessment Authority. For current versions and related content visit [www.vcaa.vic.edu.au](https://www.vcaa.vic.edu.au)**

## Learning Resources

- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- [SQL Commands Cheat Sheet](https://www.sqltutorial.org/sql-cheat-sheet/)

## Examples

### Example 1: Basic SQL Queries

```sql
SELECT * FROM students WHERE age = 17;
```

### Example 2: Creating a Database Table

```sql
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name VARCHAR(100),
    age INTEGER
);
```
