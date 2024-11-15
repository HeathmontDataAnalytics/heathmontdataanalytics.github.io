# Spreadsheets and Data Cleansing

## Overview

![Spreadsheets Image - Created by ChatGPT4o/Dall-E](/assets/images/spreadsheets.png)

Spreadsheets are powerful tools for data analysis and management. This section focuses on using spreadsheet functions for calculations, data analysis, and data cleansing. You will learn how to manipulate data using formulas and functions, sort and filter data, and identify and fix errors in data. Additionally, you will explore techniques for statistically analyzing data to identify trends, relationships, and patterns.

## Spreadsheets and Data Cleansing in the Study Design

### Unit 3 Outcome 1

**Key Knowledge:**

- design tools for representing databases and spreadsheets, including:
  - data dictionaries
  - query designs
  - layout diagrams
  - input-process-output (IPO) charts
- techniques for effectively and efficiently manipulating and cleansing data, including:
  - formulas and functions to perform calculations
  - sorting, filtering and reformatting
  - identifying and fixing errors
- techniques to statistically analyse data to identify trends, relationships and patterns, including:
  - descriptive statistics (average, median, minimum, maximum, range, standard deviation, count/frequency, sum)
  - Pearson’s correlation co-efficient (r)
  - the shape and skew of data
- techniques for testing databases and spreadsheets, including:
  - testing formula and query results
  - testing validation
  - test cases comparing expected and actual results in testing tables

  **Key Skills:**
  - manipulate and cleanse data using spreadsheet software
  - develop and apply suitable testing techniques to software tools used

### Unit 4 Outcome 1

**Key Knowledge:**

- effective and efficient methods to manipulate data using software tools, including:
  - software functions
- techniques for analysing data to refine findings for data visualisations, including:
  - descriptive statistics (average, median, minimum, maximum, range, standard deviation, count/frequency, sum)
  - Pearson’s correlation co-efficient (r)
  - the shape and skew of data

**Key Skills:**

- conduct statistical analysis to identify trends, relationships and patterns

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028.*
**© Victorian Curriculum and Assessment Authority. For current versions and related content visit www.vcaa.vic.edu.au**

## Learning Resources

- [Excel Basics for Data Analysis](https://www.microsoft.com/en-us/training)
- [Google Sheets Functions Guide](https://support.google.com/docs/answer/3093275)

## Design Tools for Spreadsheets (and Databases)

In the problem solving methodology, a Solution Design is focused on answering two key questions:

- How will my solution work? (Sometimes called the functional design)
- What will my solution look like? (Sometimes called the visual or user interface design)

To answer these questions, we use a range of design tools. For spreadsheets and databases, these tools include:

- Data Dictionaries
- Query Designs
- Layout Diagrams
- Input-Process-Output (IPO) Charts

### Data Dictionaries

A data dictionary describes the fields in a spreadsheet or database table. It includes the name of the field, the data type, and a description of the data. This helps users understand the data and how it should be used. Data dictionaries help clarify the meaning of data and ensure consistency in data entry. They may include information about the format of the data (eg. Date format, the structure of a phone number, etc.).

#### Example Data Dictionary

| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Student_ID | Number | Unique identifier for each student |
| First_Name | Text | Student's first name |
| Last_Name | Text | Student's last name |
| DOB | Date | Student's date of birth |
| Year_Level | Text | Student's year level |

## Example Exercises

### Example 1: Using Functions

- Calculate the average score of students in a class.

```excel
=AVERAGE(B2:B20)
```

### Example 2: Data Validation

- Set up a drop-down list for a column to ensure consistent data entry.
- Use conditional formatting to highlight any outliers
