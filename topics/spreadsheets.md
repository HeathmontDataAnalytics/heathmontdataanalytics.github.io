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

Data dictionaries help build the functional design of a spreadsheet or database.

#### Example Data Dictionary

| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Student_ID | Number | Unique identifier for each student |
| First_Name | Text | Student's first name |
| Last_Name | Text | Student's last name |
| DOB | Date | Student's date of birth, input as YYYY-MM-DD |
| Year_Level | Text | Student's year level |

This example could be used for a CSV file, Spreadsheet or Database table, showing the design of the fields for a student dataset.

### Query Designs

Query designs specify the criteria for selecting data from a database or spreadsheet. They define the conditions that must be met for a record to be included in the results. Query designs are used to extract specific information from a dataset based on user requirements.

#### Example Query Design

- Select all students in Year 10.
- Select students with a score greater than 80.
- Select students born after 2005.

These queries can be used to filter data in a spreadsheet or database to extract the required information.

### Layout Diagrams

Layout diagrams show the structure of a spreadsheet, or possibly the user interface to a database application. Layout diagrams help visualize the data model and understand how different elements are connected.

### Input-Process-Output (IPO) Charts

IPO charts describe the inputs, processes, and outputs of a system. In the context of spreadsheets and databases, IPO charts can be used to show how data is entered, processed, and presented to users.

- **Inputs**: Data entered into the system (whether from an external system, user input or manually added to the file). The Input of an IPO chart might show the data fields in a form or spreadsheet, or describe how the data is imported.
- **Processes**: Operations performed on the data (such as calculations, sorting, filtering, etc.). The Process of an IPO chart might show or describe the formulas going to be used in a spreadsheet, or the queries used to filter data in a database.
- **Outputs**: Results produced by the system (such as reports, visualizations, etc.). The Output of an IPO chart might describe the data visualizations or reports generated from the data.

IPO charts help in understanding the flow of data and operations in a system, and they are useful for designing and documenting the functional design of the spreadsheet or database.

## Example Exercises

### Example 1: Using Functions

- Calculate the average score of students in a class.

```excel
=AVERAGE(B2:B20)
```

### Example 2: Data Validation

- Set up a drop-down list for a column to ensure consistent data entry.
- Use conditional formatting to highlight any outliers
