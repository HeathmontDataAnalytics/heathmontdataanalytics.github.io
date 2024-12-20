# Databases and SQL

## Overview

![Database Image - Created by ChatGPT 4o](/assets/images/database.png)

Understanding databases is crucial for managing and analyzing data. This section covers relational database concepts, SQL commands, and database management.

## Main Concepts

- **Relational Database Management**: Understanding tables, primary keys, and foreign keys.
- **SQL Commands**: `SELECT`, `FROM`, `WHERE`, `JOIN`, `ORDER BY`, `GROUP BY`, `INSERT`, `UPDATE`, `DELETE`, `CREATE TABLE`, `ALTER TABLE`.
- **Large Repositories of data**: Techniques for identifying, selecting, extracting, and validating data.

## Databases in the Study Design

### Unit 3 Outcome 1

**Key Knowledge:**

- structural characteristics of relational database management systems (RDBMS), including:
  - data types and field sizes
  - data in tables
  - relationships using primary and foreign key fields
  - use of SQL to generate queries
- design tools for representing databases and spreadsheets, including:
  - data dictionaries
  - query designs
  - layout diagrams
  - input-process-output (IPO) charts
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

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028* **© Victorian Curriculum and Assessment Authority. For current versions and related content visit [www.vcaa.vic.edu.au](https://www.vcaa.vic.edu.au)**

---

### Unit 3 Outcome 1 Note

The information about design tools covers both spreadsheets and databases, so the information for the key knowledge point "design tools for representing databases and spreadsheets," has been included in the page for [Spreadsheets and Data Cleansing. Click this link to go there now.](/topics/spreadsheets.md).

---

### Unit 4 Outcome 1 Note

*While databases may be used in the Unit 4 Outcome 1 SAT task, the key knowledge and key skills do not directly mention database use.*

---

## Learning Resources

- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- [SQL Commands Cheat Sheet](https://www.sqltutorial.org/sql-cheat-sheet/)
- [Duck DB Shell Interface](https://shell.duckdb.org/)

## Relational Database Management

### What is a database?

A database is an organized collection of data, typically stored and accessed electronically from a computer system. **Relational Databases** are databases that model the data in tables with rows and columns. Each **table** represents an entity, and each **row** represents a record. The **columns** represent attributes or fields. In relational databases, tables are linked using foreign key to primary key relationships.

### Primary Key and Foreign Key Relationships

A **primary key** is a unique identifier for each record in a table. It must contain unique values and cannot be NULL. A **foreign key** is a field in a table that links to the primary key in another table. This establishes a relationship between those two tables.

For example, in an `employees` table, the `employee_id` could be the primary key. In a `departments` table, the `department_id` could be the primary key. If each employee belongs to a department, the `department_id` in the `employees` table would be a foreign key linking to the `department_id` in the `departments` table.

This means that we can retrieve all the information about each employees department (location, department name, phone number, manager, etc.) without needing to rewrite that information for each employee in the department. This is an important feature of relational databases.

### Data Types in SQL Databases

SQL database supports a variety of data types, including:

- `INTEGER`: A whole number
- `DECIMAL`, `FLOAT` or `DOUBLE`: A decimal number. Different database systems use one or more of these names, sometimes with differing levels of precision.
- `VARCHAR(n)`: A variable-length string with a maximum length of `n` (sometimes just called `TEXT`)
- `DATE`: A date value
- `TIME`: A time value
- `BOOLEAN`: A true/false value

Data types are especially important in SQL because they help ensure data integrity and accuracy. Databases will not allow data to be saved in a table unless the data type matches the column definition. This helps prevent errors and ensures that the data is consistent, but it also means that databases need to be carefully designed.

Note that the implementation of date/time data types can vary between database systems. For example, some databases store date and time together in a single data type, while others store them separately.

- In `SQLite`, you can use `TEXT` to store date and time values in the format `YYYY-MM-DD HH:MM:SS`. SQLite then provides functions to manipulate these values as dates and times.
- In `DuckDB`, you can use `DATE` and `TIME` data types to store date and time values separately.
- In `PostgreSQL`, you can use `TIMESTAMP` to store date and time values together.

### Field Sizes

As well as defining the data type of a column, you can also define the size of the column. This is particularly relevant in text fields, where you can specify the maximum number of characters that can be stored in the column. For example, a `VARCHAR(100)` column can store up to 100 characters. This ensures that data is stored efficiently and that the database is not storing more data than is necessary. It also helps to prevent errors where data is too long to be stored in a column.

## SQL

**SQL** *(Structured Query Language)* is the standard language for relational database management systems. It is used to perform tasks such as querying data, updating data, and creating databases and tables. While most database systems have tiny differences in their implementation of SQL, it is almost entirely standardized across platforms.

SQL allows you to perform a wide range of operations on a database, including selecting data, aggregating data, updating data, and deleting data from database tables. The SQL commands we study in Data Analytics are:

- `SELECT`: Retrieve data from a database
- `FROM`: Specify the table to retrieve data from
- `WHERE`: Filter data based on a condition
- `JOIN`: Combine rows from two or more tables based on a related column between them
- `ORDER BY`: Sort the result set in ascending or descending order
- `GROUP BY`: Group rows that have the same values into summary rows
- `INSERT`: Insert new records into a table
- `UPDATE`: Modify existing records in a table
- `DELETE`: Remove records from a table

Some additional commands that are useful to learn are:

- `CREATE TABLE`: Create a new table in the database
- `ALTER TABLE`: Modify an existing table in the database
- `DROP TABLE`: Delete a table from the database
- `CREATE SEQUENCE`: Create a sequence in the database
- `SUM()`, `COUNT()`, `AVG()`, `MIN()`, `MAX()`: Aggregate functions for summarizing data
- `HAVING`: Filter data after grouping has been performed

### SQL Syntax

`SELECT` statements are the most common SQL commands. The basic syntax for a `SELECT` statement is:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

This statement selects the specific columns (from the column list) from the table (specified by `table_name`) where the condition is true. The `WHERE` clause is optional, but it is used to filter the rows returned by the query.

#### SQL `SELECT` Statement Examples

- Select all columns from a `games` table:

```sql
SELECT * 
FROM games;
```

- Select specific columns from a `games` table:

```sql
SELECT game_id, title, release_date
FROM games;
```

- Select all columns from a `games` table where the `release_date` is after 2020:

```sql
SELECT *
FROM games
WHERE release_date > '2020-01-01';
```

## SQL Joins

**Joins** are used to combine rows from two or more tables based on a related column between them. There are different types of joins:

- `INNER JOIN`**`: Returns rows when there is a match in both tables.
- `LEFT JOIN` (or `LEFT OUTER JOIN`): Returns all rows from the left table and the matched rows from the right table.
- `RIGHT JOIN` (or `RIGHT OUTER JOIN`): Returns all rows from the right table and the matched rows from the left table.
- `FULL JOIN` (or `FULL OUTER JOIN`): Returns rows when there is a match in one of the tables.

In Data Analytics we primarily focus on `INNER JOIN` to combine rows from two tables where there is a match between the columns in both tables.

### SQL Join Example

Consider two tables, `employees` and `departments`, with the following columns:

`employees` table:

- `employee_id`
- `first_name`
- `last_name`
- `department_id`

`departments` table:

- `department_id`
- `department_name`
- `location`

To retrieve the `first_name`, `last_name`, and `department_name` of each employee, you could use an `INNER JOIN`:

```sql
SELECT employees.first_name, employees.last_name, departments.department_name
FROM employees
INNER JOIN departments
ON employees.department_id = departments.department_id;
```

### SQL Query Examples

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

#### Create a new table

```sql
CREATE TABLE students (
    student_id INTEGER PRIMARY KEY,
    first_name VARCHAR(100),
    last_name VARCHAR(100),
    age INTEGER
);
```

## Testing Databases

Creating queries can be a complex endeavour, especially once you get past the level of single table queries with one condition. It becomes very important to thoroughly test your queries to ensure they are returning correct results.

### Testing Principles

- **Test the Query**: Run the query and check the results.
- **Boundary Testing**: Test any `WHERE` conditions with values at the boundaries.
- **Negative Testing**: Test to makes sure that rows that should be excluded from the results do not appear.
- **Extreme Values**: Test with extreme values to ensure the query can handle them. Using values well outside the expected might allow you to find an error you didn't anticipate.
  - *For example, if you are testing a query that should return all students younger than 17, you might also test with students aged 0 and 100. If the data was being stored as text, 100 would register as being lower than 17.*

### Test Tables

One way (and the primary way in Applied Computing) of recording your test results is through the use of a test table. Test tables have four columns:

- **Feature Tested**: A description of what is being tested for in this case
- **Test Data**: The data that was used in the test. This might be the specific row in the table you are looking for in the results, or the value of a variable/parameter you are using
- **Expected Results**: What you expect to see in the results. This should be written ***before*** you run the test to avoid compromising your testing results
- **Actual Results**: What you actually see in the results. In the event the first test fails you may record multiple test runs in the Actual Results column

### Query Testing Example

Consider that Roger has been asked to retrieve the names of all students younger than 17. He writes the following query:

```sql
SELECT first_name, last_name
FROM students
WHERE age <= 17;
```

**To test this query, Roger would create a test table like this:**

| Feature Tested | Test Data | Expected Results | Actual Results |
|----------------|-----------|------------------|----------------|
| Students younger than 17 | age = 17. Table has 2 17 year old students | No students should be returned | Returned two students whose age was exactly 17 |
| Students younger than 17 | age = 16.  Table has 3 16 year old students | All students aged 16 should be returned. | Returned three students aged 16 |
| Students older than 17   | age = 18. | No students should be returned | No students were returned |
| Students aged 0          | age = 0 An additional student with an age of 0 was added for testing | 1 student aged 0 should be returned | 1 student was returned |
| Students aged 100        | age = 100 An additional student with an age of 100 was added for testing | No students should be returned | No students were returned |

The test table has helped Roger to identify that his query is not returning the correct results for the first test. He can now go back and modify his query to ensure it is returning the correct results.

## Validating Data

Validation is a core part of any computing system. We validate data to ensure that it is reasonable and appropriate for the work at hand. **Validation does not verify that the data is correct, but rather that it is reasonable.**

Across Applied Computing we have three common types of validation that we perform:

- Existence Checks: Checking whether or not something exists
- Type Checks: Checking whether or not something is the correct data type
- Range Checks: Checking whether or not something is within a certain range

Each of these forms of validation look a little different in a database.

### Existence Checks

To perform an existence check in the database, we are usually checking that data is present. In SQL this is done by using an `IS NOT NULL` or `IS NULL` statement. For example, to check that a student has a first name, you might use the following query:

```sql
SELECT * 
FROM students 
WHERE first_name IS  NULL;
```

Any rows returned would indicate student records in our database without a first name, which indicates a likely error.

Existence checks can also be performed by the primary key to foreign key relationships. For example, if we have a `students` table and a `classes` table, the foreign key constraint will make sure we only add students to classes that exist in our `classes` table.

### Type Checks

Type checks are a little more complex in SQL. SQL databases are designed to store data in a specific format, and so the database will prevent you from storing data in the wrong format. One instance where you may be required to perform type checking would be in the case of an automatically import process. In that scenario we would:

- Check that the import data is already in appropriate formats
- Verify that the created columns match our expected data types

### Range Checks

Range checks are relatively simple in an SQL database, as performing queries that filter based on a condition is a core part of SQL. For example, to check that all students are between the ages of 4 and 18, you might use the following query:

```sql
SELECT *
FROM students
WHERE age < 4 OR age > 18;
```

This would return any student records with an age outside of the expected range.

## Topic Questions

### Question 1

Why do we need a primary key in relational database tables?

### Question 2

What is the purpose of a foreign key in a relational database?

### Question 3

Describe the difference between an `INTEGER` data type and a `DECIMAL` or `FLOAT` data type in SQL. Give an example of when you might use each.

### Question 4

Hamsa is going to store the abbreviated state code (e.g., "VIC", "NSW", "WA") in a database table. She is considering using a `VARCHAR(3)` data type for this column. Is this a good choice? Why or why not?

### Question 5

Write an SQL query to select the first name, last name, and age of all students from a `students` table where the age is greater than 15.

### Question 6

What is the difference between an `INNER JOIN` and a `LEFT JOIN` in SQL?

### Question 7

Describe the purpose of the `GROUP BY` clause in SQL. Give an example of when you might use it.

### Question 8

What SQL command would you use to update someone's email address in a `users` table?

### Question 9

Delia is importing a large CSV file into a database table from a repository of weather data. The CSV has the following columns: `date`, `temperature`, `humidity`, and `wind_speed`. She wants to ensure that the data is stored correctly in the database. Describe how she could use each of the validation types on this data.

### Question 10

Explain the difference between the `WHERE` and `HAVING` clauses in SQL.

### Question 11

Michael has created a table called `games` with the following columns: `game_id`, `title`, `release_date`, and `genre`. He has set the data type of title, release_date and genre to `VARCHAR(400)`. After testing, he is confident that the database will function correctly. Why might Michael still want to reconsider the design of his database? Give two reasons.

### Question 12

Describe the results of the following SQL query:

```sql

SELECT department_name, COUNT(employee_id)
FROM departments
INNER JOIN employees
ON departments.department_id = employees.department_id
GROUP BY department_name;

```

### Question 13

Write a proposed test table (without the "Actual Results") for the query used in Question 12. Include tests for departments with no employees, departments with multiple employees, and departments with only one employee.

---
