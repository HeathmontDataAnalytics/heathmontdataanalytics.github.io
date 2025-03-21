# Unit 3 SAC Tasks

## What am I required to do?

For the Unit 3 SAC, you are provided with a set of solution requirements and designs. From this information you are required to:

- Extract a set of data from a "large repository"
- Store your extracted data in a database
- Write a set of queries using SQL
- Manipulate the extracted data using spreadsheets
- Statistically analyse the data in spreadsheets
- Create data visualisations (in accordance with the requirements) to present your findings

## Criteria

The SAC will be assessed on the following criteria (provided from VCAA):

- Interpret solution requirements and designs
- identify, select, extract and validate relevant data from a large repository
- use the APA referencing system to acknowledge intellectual property
- manipulate and cleanse data using spreadsheet software
- conduct statistical analysis to identify trends, relationships and patterns
- select, justify and apply functions, formats and conventions to create effective data visualisations
- develop and apply suitable testing techniques to software tools used

The full marking Performance Descriptors will be supplied in class.

### Part 1 - Database Solution

- **Duration:** 2 lessons (1 x double lesson)
- **Task Requirements:**
  - Extract a set of data from a "large repository"
  - Store your extracted data in a database
  - Write a set of queries using SQL to meet given requirements and design
  - Export the results of your queries to a CSV or XLSX file
  - Reference the dataset you have used in your database solution

### Part 2 - Spreadsheet Solution

- **Duration:** 2 lessons (1 x double lesson)
- **Task Requirements:**
  - Manipulate and cleanse extracted data using spreadsheets
  - Statistically analyse the data in spreadsheets

### Part 3 - Visualisation Solution

- **Duration:** 2 lessons (1 x double lesson)
- **Task Requirements:**
  - Create data visualisations (in accordance with the requirements) to present your findings

## Marking and Submission

Marking rubrics and detailed requirements will be provided in class. Your work will be submitted digitally via Compass.

The SAC as a whole will be graded at the completion of Task 3. The mark for this SAC will contribute 10% to your overall study score for Data Analytics.

## Practice SAC

For our Practice SAC we are investigating the relationship between participation in education and the economy, as measured through both population incomes and Gross Domestic Product (GDP). As part of our practice SAC we will ultimately create a data dashboard that helps respond to the following questions:

- Does a higher level of participation in education correlate with higher income?
- Does a higher level of participation in education correlate with a higher GDP?
- Do larger countries have higher levels of participation in education?

We will be using data from [Gapminder](https://www.gapminder.org/data/) to answer these questions.

### Task 1 - Database Solution

- **Duration:** 2 lessons

#### Database Task Requirements

1. Extract data from the Gapminder dataset to give you the following information:
   - Average Income
      - Country
      - Year
      - Income
   - GDP per Capita
      - Country
      - Year
      - GDP per Capita
   - An appropriate and relevant measure of participation in education
      - Country
      - Year
      - Participation in Education
   - Population
      - Country
      - Year
      - Population

2. Store your extracted data in a database. You will need to create multiple tables to store the data. Take into account the full requirements of the task to make sure you will be able to answer all the questions posed as part of the practice SAC.

3. Build a set of queries that meet the following query designs. Record the SQL query you have written, as well as a sample of the first few rows for each query. Query designs:
    1. Select all income data for a specific country
    2. Select all participation in education data for a specific country from 1980 to most recent year
    3. Select all GDP per Capita data for a specific country from 1980 to most recent year
    4. A query that compares GDP per Capita and participation in education for the most recent year across all countries
    5. A query that compares population to participation in education for the most recent year across all countries, showing NULL for any countries without data for participation in education, ordered by population descending.
    6. A query that compares average income and participation in education for the most recent year across all countries, including showing NULL for any countries that do not have data for both measures

4. Reference the Dataset you have used in your database solution.
    - Write a reference for the dataset you have used following the APA Format. You can use online referencing tools to help.

### Task 2 - Spreadsheet Solution

- **Duration:** 2 lessons

### Spreadsheet Task Requirements

1. Export the results of queries 3 & 4 from Part 1 to XLSX (Microsoft Excel) files. Save each query result in a separate, logically named file.
(If you have been unable to complete the SQL queries, Mr Matheson will provide them for you)

2. Use the supplied design tools to guide your modifications to the data. This will include:
   - Any relevant data cleansing and data validation
   - Sorting and filtering
   - Calculations to create new columns

3. Perform statistical analysis on both datasets, recording your results in accordance with the design tools. This will include:
   - Descriptive statistics: average, median, mode, range, standard deviation, with an interpretation of results
   - Correlation analysis: Pearson's correlation coefficient, with an interpretation of results
   - Analysis of shape and skew for each numerical variable, with evidence of shape

4. (Completing as you go) Write a test table with appropriate test cases for each function and validation element in your spreadsheet.

### Task 3 - Visualisation Solution

- **Duration:** 2 lessons
- **Task Requirements:**

1. Create a data dashboard in line with this [layout diagram provided](/assets/files/layout_diagram_visualisation.pdf) using Streamlit and the following files:
   - [gdp_pop_primary.csv](/assets/files/gdp_pop_primary.csv) - GDP per Capita, Population, and Primary Education Participation from the spreadsheet solution
   - [gdp_pop_summary.csv](/assets/files/gdp_pop_summary.csv) - GDP per Capita and Population Summary Statistics from the spreadsheet solution
   - [primary_country_time.csv](/assets/files/primary_country_time.csv) - Primary Education Participation by Country and Year from the database solution

2. Write a justification for the choices you made in creating this visualisation.
   - What makes this an effective data visualisation?
   - How do your choice of colours, charts, and statistics help to communicate meaningful information?

3. Write a test table with appropriate test cases for each function and validation element in your visualisation. Include test cases for:
   - Each of the charts
   - Each of the statistics
   - Interactive elements

Submit your streamlit file (app.py) and your test table and justification to the learning task on Compass.
