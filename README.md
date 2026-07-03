# AtliQ-Virtual-Internship-Week-1-july-2026

Welcome to my AtliQ Technologies Virtual Internship project. This repository features a data cleaning and business analysis solution built for AtliQ Technologies' HR attendance data, along with a data normalization solution built for AtliQ Technologies' order level sales data. The project utilizes Power Query-based data cleaning, DAX-driven analysis, and star schema data modeling to evaluate key workforce metrics and structure denormalized transactional data for reliable reporting.

---

## Table of Contents
- [Introduction](#introduction)
- [Project Description](#project-description)
- [Folder Structure](#Folder-Structure)
- [Key Features](#Key-Features)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Introduction
---
*Project Title:* AtliQ Technologies Virtual Internship, Week 1  
*Created By:* [Sachin-Analyst](https://github.com/Sachin-Analyst)  
*Tools Used:* Power BI, Excel, Power Query, Power Pivot, DAX  
*Focus Areas:* Data Cleaning & Standardization, Workforce Attendance Analysis, WFH Trend Evaluation, Data Normalization, Star Schema Modeling

---

## Project Description
This repository contains the Week 1 body of work from my Data Analyst Virtual Internship at AtliQ Technologies.

*Task 1* covers cleaning a raw HR attendance dataset in Power Query fixing duplicates, inconsistent date formats, stray characters in employee IDs, inconsistent name capitalization, and unmapped status codes — followed by DAX-based analysis to answer real business questions on employee count, WFH percentage, and attendance trends.


*Task 2* covers transforming a denormalized order-level dataset (`fact_order_lines.csv`) into a normalized star schema using Power Query and Power Pivot in Excel splitting a single flat table into one fact table and three dimension tables (customers, products, date), connected via Diagram View relationships.


Task 3 will be added to this repository as the week progresses.

---

## Folder Structure
- *Task-1* - Cleaning & Analyzing Employee Dataset: full Power Query steps and DAX measures used, with real problem/approach/result documentation
- *Task-2* - Normalizing Denormalized Order Data: full breakdown of the Reference-based star schema build, from staging query to final relationships
- *Task-3* - Coming soon

## Key Features
- *Data Cleaning* - duplicate removal, date standardization, employee ID cleanup, name capitalization, status code mapping
- *Workforce Attendance Analysis* - distinct employee count, monthly WFH % calculation, attendance trend by day of week
- *DAX-Driven Business Answers* - real business questions answered using validated DAX measures
- *Data Normalization* - denormalized flat table split into a star schema (1 fact table + 3 dimension tables) using Power Query References
- *Relationship Modeling* - dimension-to-fact relationships built in Power Pivot Diagram View on natural keys

## Installation
To explore or modify this project:
1. *Clone the repository:*
```bash
   git clone https://github.com/Sachin-Analyst/AtliQ-Virtual-Internship-Week-1.git
```
   - Open terminal and run the command
2. *Download and Open Power BI Desktop or Excel*
   - Task 1 was built using Power BI Desktop with Power Query and DAX
   - Task 2 was built using Excel with Power Query and Power Pivot
3. *Explore Resources*
   - Open the Task-1 folder to review the full breakdown of cleaning steps and DAX measures used
   - Open the Task-2 folder to review the full breakdown of the normalization process and star schema

---

## Usage
### What You Can Explore
- Power Query steps used to clean a real-world messy HR dataset
- DAX measures for distinct counts, percentage calculations, and conditional filtering
- Real results for each business question answered
- Power Query steps used to split a denormalized dataset into a star schema
- The reasoning behind choosing Reference over Duplicate when branching queries

----
### Explore the `Task-1` folder for the full breakdown and business logic behind each requirement.
### Explore the `Task-2` folder for the full breakdown of the normalization process, from staging query to final relationships.
----

# Note !
The raw datasets used in this project are internal to the AtliQ Technologies internship program and are not included in this repository. All logic and results shown are based on those datasets.

----

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
