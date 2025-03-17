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
  - Pearson's correlation co-efficient (r)
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
  - Pearson's correlation co-efficient (r)
  - the shape and skew of data

**Key Skills:**

- conduct statistical analysis to identify trends, relationships and patterns

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028.*
**© Victorian Curriculum and Assessment Authority. For current versions and related content visit www.vcaa.vic.edu.au**

## Learning Resources

- [Excel Basics for Data Analysis](https://support.microsoft.com/en-au/office/basic-tasks-in-excel-dc775dd1-fa52-430f-9c3c-d998d1735fca)
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

Layout diagrams are used in Data Analytics to show the structure of a spreadsheet, or possibly the user interface to a database application. Layout diagrams help visualize the data model and understand how different elements are connected. They can include information about the layout of data fields, tables, and relationships between them.

### Input-Process-Output (IPO) Charts

IPO charts describe the inputs, processes, and outputs of a system. In the context of spreadsheets and databases, IPO charts can be used to show how data is entered, processed, and presented to users.

- **Inputs**: Data entered into the system (whether from an external system, user input or manually added to the file). The Input of an IPO chart might show the data fields in a form or spreadsheet, or describe how the data is imported.
- **Processes**: Operations performed on the data (such as calculations, sorting, filtering, etc.). The Process of an IPO chart might show or describe the formulas going to be used in a spreadsheet, or the queries used to filter data in a database.
- **Outputs**: Results produced by the system (such as reports, visualizations, etc.). The Output of an IPO chart might describe the data visualizations or reports generated from the data.

IPO charts help in understanding the flow of data and operations in a system, and they are useful for designing and documenting the functional design of the spreadsheet or database.

#### Example IPO Chart

| Input | Process | Output |
|------------|-----------|-------------|
| Recorded Temperatures from Bureau of Meteorology | Calculate Average, Maximum and Minimum temperatures across each month | Summary Table for each month  |
| | | Line graph showing temperature trends |

This IPO chart describes the process of analyzing temperature data to create a summary table and a line graph.

## Data Cleansing

Data cleansing is the process of identifying and correcting errors in a dataset. It involves removing or correcting inaccurate, incomplete, or irrelevant data to improve the quality and reliability of the data. It may include solving problems caused by an incorrect data type or Data cleansing is essential for accurate analysis and decision-making.

## Techniques for Manipulating and Cleansing Data

### Formulas and Functions

Formulas and functions are essential tools for manipulating data in spreadsheets. They allow you to perform calculations, apply logical operations, and transform data. Common functions include SUM, AVERAGE, IF, VLOOKUP, and CONCATENATE.

## Descriptive Statistics

Descriptive statistics are used to describe the basic features of the data in a study. They provide simple summaries about the sample and the measures. Together with simple graphics analysis, they form the basis of virtually every  analysis of data.

The descriptive statistics we study fall into three categories:

- Measures of Central Tendency (Averages)
  - Average (Mean)
  - Median
- Measures of Spread (Variability)
  - Minimum & Maximum
  - Range
  - Standard Deviation
- Measures of Size (Frequency)
  - Count
  - Sum

Each of these measures is applied to numerical data to provide a summary of the data set.

## Average and Median

### Average (Mean)

- Described in Applied Computing as Average, but mathematically as the mean.
- The sum of all values divided by the number of values.
- The most common measure of central tendency.
- Can be affected by outliers
  - Which may not be representative of the data set
- Can be calculated using the `AVERAGE` function in Excel eg. `=AVERAGE(A1:A10)`

### Median

- The middle value of a data set.
- The median is not affected by outliers.
- Can be calculated using the `MEDIAN` function in Excel eg. `=MEDIAN(A1:A10)`
- If there are an even number of values, the median is the average of the two middle values.
- Also represents the 50th percentile of the data set.

## Minimum and Maximum

### Minimum

- The smallest value in a data set.
- Can be calculated using the `MIN` function in Excel eg. `=MIN(A1:A10)`
- Can be used to identify the range of values in a data set.

### Maximum

- The largest value in a data set.
- Can be calculated using the `MAX` function in Excel eg. `=MAX(A1:A10)`
- Can be used to identify the range of values in a data set.

## Range and Standard Deviation

Measures of spread (such as range and standard deviation) provide information about the variability of the data set. Two data sets could have very similar averages but very different ranges or standard deviations, indicating that one data set is more spread out than the other.

### Range

- The difference between the maximum and minimum values in a data set.
- Can be calculated using the `MAX` and `MIN` functions in Excel eg. `=MAX(A1:A10) - MIN(A1:A10)` (Not able to be calculated on its own)
- Provides a measure of the spread of the data set.
- Can be affected by outliers.

### Standard Deviation

- A measure of the amount of variation or dispersion of a set of values.
- Can be calculated using the `STDEV` function in Excel eg. `=STDEV(A1:A10)`
- The standard deviation is the square root of the variance.
- The variance is the average of the squared differences from the mean.
- Can be affected by outliers.

## Count and Sum

Count and sum are measures of size. Count provides the number of values in a data set, while sum provides the total of all values in a data set. It is important to consider whether the sum or count is relevant for the particular data values being analysed. If you cannot explain what the sum or count represents, it is not useful.

### Count

- The number of values in a data set.
- Can be calculated using the `COUNT` function in Excel eg. `=COUNT(A1:A10)`. This counts the number of cells in a range that contain numbers (ignores empty cells).
- Can be used to identify missing data.
- Can be used to identify the size of a data set.

### Sum

- The total of all values in a data set.
- Can be calculated using the `SUM` function in Excel eg. `=SUM(A1:A10)`
- Can be used to identify the total of a data set.

## Pearson's Correlation Coefficient (r)

Pearson's correlation coefficient (r) is a measure of the strength and direction of the linear relationship between **two numeric variables**. It ranges from -1 to 1, where:

- 1 indicates a perfect positive linear relationship
- -1 indicates a perfect negative linear relationship
- 0 (or between -0.25 and 0.25) indicate no linear relationship
- Values close to 1 or -1 indicate a strong linear relationship

Pearson's correlation coefficient is calculated using the `CORREL` function in Excel. For example, `=CORREL(A1:A10, B1:B10)` calculates the correlation between two sets of values in columns A and B.

## Strength and Direction of Relationships

### Strength

- The strength of a relationship between two variables is determined by the value of r.
- Values close to 1 or -1 indicate a strong linear relationship.
- Strength can be described as:
  - Strong: r > 0.75 or r < -0.75
  - Moderate: 0.5 < r < 0.75 or -0.75 < r < -0.5
  - Weak: 0.25 < r < 0.5 or -0.25 > r > -0.5
  - No relationship: -0.25 < r < 0.25
- The strength of a relationship can be affected by outliers.

### Direction

- The direction of a relationship is determined by the sign of r.
- A positive value of r indicates a positive linear relationship.
- A negative value of r indicates a negative linear relationship.
