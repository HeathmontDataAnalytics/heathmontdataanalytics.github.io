# Project Management Strategies

## Overview

Effective project management is essential for delivering successful data projects. This section covers planning techniques, Gantt charts, and tracking progress.

## Key Concepts

- **Gantt Charts**: Visualizing tasks and timelines.
- **Milestones**: Setting key goals and deadlines.
- **Critical Path**: Identifying the tasks which can run concurrently and which tasks will delay the whole project if they are delayed themselves
- **Risk Management**: Identifying and mitigating project risks.

## Learning Resources

- [Gantt Chart Basics](https://www.smartsheet.com/gantt-chart)

## Example Exercises

### Exercise 1: Creating a Gantt Chart

- Create a simple Gantt chart for a data analysis project using Excel or Google Sheets.

### Exercise 2: Identifying Project Risks

- List potential risks for a data visualisation project and propose mitigation strategies.

```mermaid
    gantt
    title SAT Project Template
    dateFormat DD/MM/YYYY
    excludes weekends, Wednesday, Friday

    section Unit 3 - Analysis
    Project Start               :milestone, a1, 01/02/2025, 1d
    Identify Research Question  : done, a2, after a1,  5d
    Create project plan         : done, a3, after a2, 2d
    Gather requirements         : active, a4, after a2, 5d 
    Analysis Complete           : milestone, after a3 a4, 1d

    section Unit 3 - Design
    System Design               : d1, 01/04/2025, 10d
    Evaluation Criteria created : d2, after d1, 5d
    Design Ideas                : d3, after d2, 4d
    Design Complete             : milestone,  dm, after d4, 0d

    section Unit 4 - Development
    Start Unit 4                : milestone, devstart, 20/07/2025, 1d
    Create Data Visualisation   : dev1, after devstart, 12d
    Testing                     : dev2, after dev1, 3d
    Finalised                   : milestone, devm, after dev2, 0d

    section Unit 4 - Evaluation
    Start Evaluation            : e1, after devm, 3d
    Generate Eval Strategy      : e2, after e1, 3d
```
