# HR Employee Attrition Analytics Dashboard

An interactive Excel dashboard that breaks down employee attrition by department, job role, overtime, business travel, work-life balance, age, and income — so HR questions can be answered by filtering the data instead of reading a static report.

## Overview

This project analyzes an HR dataset of **1,480 employees** across **3 departments** and **9 job roles** to understand where and why attrition happens. Instead of a single "attrition rate" number, the dashboard is built to let a user drill from a company-wide view down to department- and employee-level patterns, using slicers to filter by the factors that matter — overtime, travel, work-life balance, age, salary band, and more.

## Business Problem

A single overall attrition rate doesn't tell HR what to fix. This dashboard was built to answer:

- Is attrition concentrated in specific departments or job roles?
- Does working overtime increase the likelihood of an employee leaving?
- Does business travel frequency correlate with attrition?
- Does self-reported work-life balance predict attrition?
- How does income compare across departments and by gender?
- How does tenure (years at company) vary by job role?

## Dataset

The dataset contains 1,480 employee records with fields including:

- **Demographics:** Age, Gender, Marital Status, Education Field
- **Employment:** Department, Job Role, Years at Company, OverTime, Business Travel
- **Compensation:** Monthly Income, Salary Slab
- **Attrition & Satisfaction:** Attrition (Yes/No), Job Satisfaction Score, Work-Life Balance rating
- **Career Progression:** Years Since Last Promotion, Years in Current Role

## Objectives

- Calculate overall attrition rate and identify its key drivers
- Compare attrition across departments and job roles
- Test whether overtime and business travel correlate with attrition
- Examine the relationship between work-life balance and attrition
- Compare income across departments and gender
- Analyze tenure (years at company) patterns by job role

## Tools & Technologies

- **Microsoft Excel**
- **Power Query** for data cleaning and transformation, including building calculated columns such as Age Group and Work-Life Balance category labels (e.g. Better, Good, Best, Poor)
- **PivotTables** and **PivotCharts** for aggregation and visualization
- **Slicers** for interactive, cross-filtered exploration
- Custom dashboard design (dedicated color/theme reference sheet, KPI card layout, treemap and bar/line chart visualizations)

## Dashboard Pages

### OverView
The company-wide summary page. **KPIs:** Attrition Rate (16%), Overtime Rate (28%), Average Monthly Income ($6,504.99). **Charts:** Attrition Rate by Job Roles, Average Monthly Income by Department, Satisfaction Rate by Job Role (treemap), Attrition Rate by Age, Employee Distribution by Department. **Filters:** Age Group, Department, Salary Slab.

### Department
Focused on where attrition concentrates operationally. **KPIs:** Number of Departments (3), Number of Job Roles (9), Attrition Rate (16%). **Charts:** Attrition Rate by OverTime, Attrition Rate by Business Travel, Satisfaction Rate by Department, Attrition Rate by Work-Life Balance, Average Years at Company by Job Role. **Filters:** Marital Status, Department, Business Travel.

### Employee
Focused on individual-level patterns. **KPIs:** Total Employees (1,480), OverTime Employees (418), Satisfaction Score (2.73/4). **Charts:** Attrition Rate by Years Since Last Promotion, Monthly Income by Age Group, Male vs Female (headcount and average income), Attrition Rate by Years at Current Role. **Filters:** Education Field, Department, Gender.

## Key Insights

- **Overall attrition rate is 16%**, with an average monthly income of $6,504.99 across the company.
- **Overtime is strongly linked to attrition**: employees who work overtime leave at a **31%** rate, versus **10%** for those who don't — roughly 3x higher.
- **Business travel frequency correlates with attrition**: Non-Travel employees show **8%** attrition, Travel Rarely **15%**, and Travel Frequently **25%**.
- **Work-life balance tracks closely with attrition**: Better (**14%**), Good (**17%**), Best (**18%**), Poor (**31%**).
- **Sales Representative has the highest attrition of any job role at 39%**, well above the next-highest role (Sales Executive, 18%).
- **Satisfaction by department** is fairly even: Sales (29%), Research & Development (28%), Human Resources (27%).
- **Average monthly income by department**: Sales ($6,966.74), Human Resources ($6,654.51), Research & Development ($6,280.37).
- **Gender income comparison**: Male employees (889) average $6,385.71/month; Female employees (591) average $6,684.40/month.
- **Tenure varies widely by job role**, from Sales Representative (2.93 years average) to Manager (14.43 years average).
- **Employee distribution by department**: Research & Development (967), Sales (450), Human Resources (63).

## Key KPIs

| KPI | What it measures |
|---|---|
| Attrition Rate | Share of employees who have left the company |
| Overtime Rate | Share of employees who regularly work overtime |
| Average Monthly Income | Company-wide average monthly income |
| Number of Departments / Job Roles | Structural size of the organization |
| Total Employees | Total headcount in the dataset |
| OverTime Employees | Count of employees who work overtime |
| Satisfaction Score | Average self-reported job satisfaction (scale of 4) |

## Interactivity

Each dashboard page includes slicers relevant to its focus, so any chart or KPI can be filtered live:

- **OverView:** filter by Age Group, Department, or Salary Slab
- **Department:** filter by Marital Status, Department, or Business Travel
- **Employee:** filter by Education Field, Department, or Gender

A "Clear Filters" control resets all slicers on a page back to the full dataset view.

## Data Preparation

- Used **Power Query** to import and clean the source data.
- Created calculated columns not present in the raw data, including **Age Group** (banding employees into ranges such as 18–25, 26–35, etc.) and **Work-Life Balance category labels** (Better, Good, Best, Poor).
- Built PivotTables on the cleaned data to power the dashboard's PivotCharts, KPIs, and slicers.

*(Add any further cleaning steps — e.g. handling missing values or standardizing other categorical labels — if you performed them.)*

## Insights & Recommendations

**What the data shows:**
- Overtime, business travel frequency, and work-life balance are all associated with higher attrition in this dataset.
- Sales Representative has a disproportionately high attrition rate compared to every other role.
- Female employees in this dataset have a higher average monthly income than male employees.

**Recommendations based on the above (not directly shown by the data, but a reasonable response to it):**
- Investigate overtime policy and workload distribution, particularly in roles and departments with high overtime rates, given the strong association with attrition.
- Review travel requirements for frequent-travel roles and consider whether travel frequency can be reduced or better compensated.
- Prioritize a retention review for the Sales Representative role specifically, since its attrition rate is far outside the norm for the organization.
- Use work-life balance scores as an early-warning signal — employees rating it "Poor" are leaving at more than double the rate of those rating it "Better."

## Project Structure

```
hr-attrition-dashboard/
├── README.md
├── HR_Attrition_Dashboard.xlsx
├── screenshots/
│   ├── 01-overview.png
│   ├── 02-department.png
│   └── 03-employee.png
└── LICENSE
```

## How to Use

1. Download `HR_Attrition_Dashboard.xlsx`.
2. Open it in Microsoft Excel (2016 or later recommended, for full chart compatibility).
3. Navigate between the OverView, Department, and Employee tabs using the in-sheet navigation buttons at the top of each page.
4. Use the slicers on the right of each page to filter the dashboard — for example, select a single department or age group to see all charts and KPIs update accordingly.
5. Use "Clear Filters" to reset a page to its full, unfiltered view.

## Screenshots

**OverView**
<img width="1797" height="660" alt="Screenshot 2026-09-05 171409" src="https://github.com/user-attachments/assets/987eaa33-c800-4a49-a183-f2dbddc915d7" />

*Company-wide KPIs and attrition breakdown by job role, department income, and job-role satisfaction.*

**Department**
(screenshots/02-department.png)<img width="1757" height="657" alt="Screenshot 2026-09-05 171429" src="https://github.com/user-attachments/assets/f4b7e83e-9ad0-439c-9e6c-ebcb29a41cc8" />

*Attrition rate by overtime, business travel, and work-life balance — the dashboard's core diagnostic view.*

**Employee**
![Employee dashboard](screenshots/03-employee.png)<img width="1743" height="656" alt="Screenshot 2026-09-05 171454" src="https://github.com/user-attachments/assets/9c112403-662d-466d-84c1-028fe2500464" />

*Individual-level patterns: attrition by years since last promotion and years in current role, income by age group, and gender comparison.*

## Future Improvements

- Bucket the Years Since Last Promotion and Years at Current Role attrition line charts into ranges (similar to the existing Age Group buckets) for cleaner, less noisy trend lines.
- Add a direct chart comparing average income or tenure between employees who left and employees who stayed.
- Rebuild the dashboard in Power BI to add native drill-through and faster cross-filtering.
- Add a predictive element (e.g., a simple attrition risk score) as a follow-up project.

## Author

**Sama Ahmed**
