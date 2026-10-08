# Excel Salary Dashboard
 
## Introduction
 
This Data Jobs Salary Dashboard was created to help job seekers explore salary trends for their target roles and determine whether they are being competitively compensated.
 
The dashboard is based on data from my Excel course and demonstrates how Excel can be used to analyze and visualize real-world salary information. The dataset includes job titles, salaries, locations, and key skills, which are presented through an interactive dashboard.
 
---
 
## Dashboard File
 
📂 **Salary_Dashboard.xlsx**
 
---
 
## Excel Skills Used
 
The following Excel skills were utilized in this project:
 
- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation
 
---
 
## Data Jobs Dataset
 
The dataset contains real-world Data Science job information from 2023 and includes:
 
- 👨‍💼 Job Titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills
 
---
 
# Dashboard Build
 
## 📉 Charts
 
### 📊 Data Science Job Salaries - Bar Chart
 
**Excel Features Used**
- Created a horizontal bar chart with formatted salary values.
- Optimized layout for clarity and readability.
 
**Design Choice**
- Used a horizontal bar chart to enable easy salary comparisons across job titles.
 
**Data Organization**
- Sorted job titles in descending order of median salary.
 
**Key Insight**
- Senior and Engineering roles generally offer higher salaries compared to Analyst positions.
 
---
 
### 🗺️ Country Median Salaries - Map Chart
 
**Excel Features Used**
- Leveraged Excel's Map Chart feature to visualize global median salaries.
 
**Design Choice**
- Used color coding to differentiate salary levels across countries.
 
**Data Representation**
- Displayed median salary data for all available countries.
 
**Visual Enhancement**
- Improved readability and provided an immediate understanding of geographic salary trends.
 
**Key Insight**
- Highlights global salary disparities and identifies regions with comparatively higher and lower compensation.
 
---
 
## 🧮 Formulas and Functions
 
### 💰 Median Salary by Job Title
 
```excel
=MEDIAN(
IF(
(jobs[job_title_short]=A2)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
(jobs[salary_year_avg]<>0),
jobs[salary_year_avg]
)
)
```
 
**Purpose**
 
- Applies multiple filtering criteria:
- Job Title
- Country
- Schedule Type
- Non-blank Salary Values
 
- Uses an array formula combining `MEDIAN()` and `IF()` functions.
- Returns the median salary based on user-selected criteria.
- Populates the salary table displayed in the dashboard.
 
---
 
### ⏰ Count of Job Schedule Type
 
```excel
=FILTER(
J2#,
(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))
*(J2#<>0)
)
```
 
**Purpose**
 
- Generates a filtered list of unique job schedule types.
- Removes entries containing:
- "and"
- ","
- Zero values
 
- Serves as the source data for dashboard filters.
 
---
 
## ❎ Data Validation
 
### 🔍 Filtered List Validation
 
Implemented Data Validation for:
 
- Job Title
- Country
- Schedule Type
 
### Benefits
 
- 🎯 Restricts user input to valid options
- 🚫 Prevents inconsistent entries
- 👥 Enhances dashboard usability
- 🔒 Improves data quality and accuracy
 
---
 
# Dashboard Features
 
- Interactive filtering by Job Title, Country, and Schedule Type
- Salary comparison across data-related roles
- Global salary visualization using Map Charts
- Dynamic calculations powered by Excel formulas
- User-friendly dashboard navigation
 
---
 
# Conclusion
 
This dashboard was developed to analyze salary trends across various data-related careers using Excel.
 
By combining charts, formulas, and data validation techniques, the dashboard enables users to:
 
- Compare salaries across job roles
- Explore geographical salary variations
- Understand the impact of employment type on compensation
- Make more informed career decisions
 
This project demonstrates practical Excel dashboarding techniques while providing valuable insights into the Data Science job market.
