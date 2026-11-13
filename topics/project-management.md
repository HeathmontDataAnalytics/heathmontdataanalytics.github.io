# Project Management Strategies

## Overview

![Project Management Image - Created by ChatGPT4o/Dall-E](/assets/images/projectmanagement.png)

Effective project management is essential for delivering successful data projects. This section covers planning techniques, Gantt charts, and tracking progress. Lots of our focus for the project management is on tracking the progress of our SAT project and associated tasks.

## Key Concepts

- **Gantt Charts**: A chart showing each task as a bar against a timeline, so you can see when tasks start and finish and how they relate to each other.
- **Tasks**: The individual pieces of work that make up the project.
- **Dependencies**: Tasks that cannot start until another task has finished.
- **Milestones**: Significant points in the project, such as a SAT submission. A milestone takes no time.
- **Critical Path**: The longest sequence of dependent tasks through the project. If any task on the critical path is delayed, the whole project is delayed.
- **Risk Management**: Identifying and mitigating project risks.

## Project Management in the Study Design

### Unit 3 Outcome 2

**Key Knowledge:**

- features of project management to develop a project plan using Gantt charts, including:
  - identification of tasks
  - sequencing of tasks
  - time allocation
  - dependencies
  - milestones
  - critical path
  - monitoring and documenting the progress of projects

**Key Skills:**

- create, monitor and modify project plans using software

### Unit 4 Outcome 1

**Key Knowledge:**

- techniques for recording the progress of projects, including:
  - adjustments to tasks
  - adjustments to time frames
  - annotations to project plans
  - monitoring and documenting progress using logs/journals
- techniques for assessing the effectiveness of a project plan, including:
  - reviewing the number of changes made to the project plan during the project
  - the reason changes were necessary
  - the impact of changes on the completion of the project.

**Key Skills:**

- monitor, modify and annotate project plans as necessary
- assess the effectiveness of the project plan

*Study design key knowledge and key skills are taken verbatim from the VCE Applied Computing Study Design 2025-2028.*
**© Victorian Curriculum and Assessment Authority. For current versions and related content visit [www.vcaa.vic.edu.au](https://www.vcaa.vic.edu.au)**

## Learning Resources

- [Gantt Chart Basics](https://www.smartsheet.com/gantt-chart)
- [SAT Overview](/assessments/sat.md) - the project plan is part of the first Unit 3 SAT submission

## Features of a Project Plan

A project plan sets out everything that needs to be done to complete a project, in what order, and how long each part should take. For the SAT, your project plan is a Gantt chart that covers all stages of the problem-solving methodology across Unit 3 Outcome 2 and Unit 4 Outcome 1. It must include both the milestones your teacher gives you (such as submission dates) and milestones you set for yourself.

### Identification of Tasks

The first step is to break the project down into tasks. A task should be a single, clear piece of work that you can tell is finished. Tasks that are too large ("Do the SAT") are impossible to schedule or monitor, while tasks that are too small ("Open Excel") make the plan cluttered.

Good tasks usually start with a verb and describe a result, for example:

- *Find and download GDP and life expectancy data from Gapminder*
- *Write functional and non-functional requirements*
- *Create three design ideas using mood boards and sketches*

It helps to group your tasks by the stage of the problem-solving methodology they belong to (analysis, design, development and evaluation).

### Sequencing of Tasks

Sequencing means putting the tasks in the order they need to be done. Some tasks have to happen in a set order (you cannot clean data you have not collected yet), while others can happen at the same time (concurrently). Getting the sequence right means you are never waiting around for something you could have started earlier.

### Time Allocation

Each task is given an estimated duration, usually in days or lessons. Be realistic: think about how many lessons you have each week, other assessments, and how long similar tasks have taken you in the past. It is common to underestimate how long tasks will take, especially data collection and cleansing. Leaving a little extra time on important tasks gives you room if things go wrong.

### Dependencies

A dependency is a relationship between two tasks where one task relies on another. The most common type is **finish-to-start**: task B cannot start until task A is finished. For example, *Clean data* depends on *Collect data*.

On a Gantt chart, dependencies are often shown as arrows from the end of one task to the start of the next. Identifying dependencies is what allows you to work out the critical path.

### Milestones

A milestone marks a significant point in the project, such as completing a stage or submitting part of the SAT. Milestones have **no duration**; they are a point in time rather than a task, and are usually shown on a Gantt chart as a diamond. Milestones make it easy to check whether you are on track: if you reach a milestone late, you know the project is behind schedule.

### Critical Path

The critical path is the longest chain of dependent tasks from the start of the project to the end. It tells you the shortest possible time the project can take. Any delay to a task on the critical path delays the entire project.

Tasks **not** on the critical path have **slack** (also called float): they can be delayed by a certain amount without delaying the project.

#### Critical Path Worked Example

| Task | Description | Duration (days) | Depends on |
|------|-------------|-----------------|------------|
| A | Choose research question | 3 | - |
| B | Find secondary data sources | 4 | A |
| C | Write requirements, constraints and scope | 3 | A |
| D | Collect and clean data | 5 | B |
| E | Create design ideas | 4 | C |
| F | Produce detailed design | 3 | D, E |

There are two paths from the start of the project to the end:

- **A → B → D → F**: 3 + 4 + 5 + 3 = **15 days**
- **A → C → E → F**: 3 + 3 + 4 + 3 = **13 days**

The longest path is **A → B → D → F**, so this is the critical path and the project will take at least 15 days. Tasks C and E have **2 days of slack**: they could both run 2 days late without delaying task F. If task D (collecting and cleaning data) runs 2 days late, however, the whole project finishes 2 days late.

### Monitoring and Documenting Progress

A project plan is not something you create once and forget. Throughout the SAT you should regularly compare your actual progress against the plan:

- Mark tasks as complete, in progress, or not started
- Record when tasks actually started and finished, compared with what was planned
- When things change, modify the plan (adjust tasks or timeframes) and record **why** the change was needed

Keeping a record of these changes, for example in a log or journal, is important because in Unit 4 you will need to assess how effective your project plan was.

## Gantt Charts

A Gantt chart displays tasks as horizontal bars along a timeline. The position of a bar shows when a task starts, and its length shows its duration. Gantt charts make it easy to see sequencing, dependencies, concurrent tasks and milestones at a glance. You do not need dedicated project management software; a spreadsheet works well.

The [SAT Project Template](#sat-project-template) at the end of this page is an example Gantt chart for the SAT project. Tasks are grouped into sections by stage of the problem-solving methodology. Milestones mark the start and end of each stage, and the `after` keyword shows dependencies. For example, *Analysis Complete* cannot occur until both *Create project plan* and *Gather requirements* are finished. Tasks marked done and active show how the chart can be updated to monitor progress.

## Examples

### Example 1: Creating a Gantt Chart

Using the tasks in the critical path worked example above, create a Gantt chart in a spreadsheet:

1. List each task in column A and its duration in column B.
2. Calculate a start date for each task based on its dependencies (a task starts when the last task it depends on finishes).
3. Use a stacked bar chart (or conditional formatting across a row of dates) to show each task as a bar.
4. Add milestones for *Analysis Complete* and *Design Complete*.
5. Highlight the tasks on the critical path in a different colour.

### Example 2: Identifying Project Risks

List at least three potential risks for a data visualisation project and propose a mitigation strategy for each. For example:

| Risk | Mitigation strategy |
|------|---------------------|
| The data needed to answer the research question cannot be found | Check data is available before finalising the research question |
| Survey responses are slower to come in than expected | Send the survey early and set a closing date with time to spare |
| Data loss due to a corrupted file | Keep regular backups in more than one location |

### SAT Project Template

<pre class="mermaid">
gantt
title SAT Project Template
dateFormat DD/MM/YYYY
excludes weekends, Wednesday, Friday

section Unit 3 - Analysis
Project Start : milestone, a1, 01/02/2025, 0d
Identify Research Question : done, a2, after a1, 5d
Create project plan : done, a3, after a2, 2d
Gather requirements : active, a4, after a2, 5d
Analysis Complete : milestone, a5, after a3 a4, 0d

section Unit 3 - Design
System Design : d1, 01/04/2025, 10d
Evaluation Criteria created : d2, after d1, 5d
Design Ideas : d3, after d2, 4d
Design Complete : milestone, dm, after d3, 0d

section Unit 4 - Development
Start Unit 4 : milestone, devstart, 20/07/2025, 0d
Create Data Visualisation : dev1, after devstart, 12d
Testing : dev2, after dev1, 3d
Finalised : milestone, devm, after dev2, 0d

section Unit 4 - Evaluation
Start Evaluation : e1, after devm, 3d
Generate Eval Strategy : e2, after e1, 3d
</pre>

<script type="module">
  import mermaid from "https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs";
  mermaid.initialize({ startOnLoad: true });
</script>

## Topic Questions

### Question 1

What is the difference between a task and a milestone? Give an example of each from the SAT.

### Question 2

Explain what is meant by a dependency between two tasks. Give an example of two SAT tasks where one depends on the other.

### Question 3

Using the critical path worked example above, task E (*Create design ideas*) takes 5 days instead of 4. Does this change the finish date of the project? Explain why or why not.

### Question 4

In the same example, task B (*Find secondary data sources*) takes 6 days instead of 4. What happens to the critical path and the total project duration?

### Question 5

Explain why it is important to record the reasons for changes made to your project plan during the SAT.

### Question 6

Identify the tasks, durations and dependencies for the analysis stage of your own SAT, and use them to create a Gantt chart that shows the critical path.
