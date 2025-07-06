# DSA-DATA-ANALYSIS-CAPSTONE-PROJECT-PALMORIA-GROUP
This Power BI dashboard delivers an in- depth HR Analysis for Palmoria Group, which reveals gender, salary, and performance disparities across regions amid public scrutiny, guiding leadership on equity and compliance improvements.

## Case Study 2: Palmoria Group HR Review Analysis 

### Project Overview
This Data Analysis project showcases a comprehensive HR analytics case study conducted for Palmoria Group, a Nigerian manufacturing company under public scrutiny for gender imbalance and compensation disparities within its workforce. Sparked by a damaging media headline “Palmoria, the Manufacturing Patriarchy” the company’s leadership initiated a strategic push toward equity and transparency.
As the HR Analytics Lead, I conducted a detailed, data-driven investigation into critical HR issues across three regional locations, focusing on:
 - Gender distribution and workforce diversity
 - Salary structure and pay equity
 -  Employee performance metrics
 - Regulatory and compliance alignment.

The project aims to drive accountability, foster workplace inclusivity, and guide Palmoria Group toward sustainable HR practices.

### Dataset Used
The primary sources of data used here is Palmoria  Group emp-data.csv and Palmoria Group Bonus Rules.xlsx and this is an open source data that can be freely downloaded from an open source online such as Kaggle or FRED or any other data repository site.

### Tools Used:
- Power BI Desktop for data modeling and visualization
- Power Query Editor for cleaning and transformation
- DAX for calculated measures (bonus, salary + bonus, compliance checks
- Excel for supplementary bonus rule data

### Process : Data Cleaning & Preparation
Before analysis, the HR dataset underwent ETL process -Extract, Transform and Load :
- Employees who refused to disclose their gender were classified under a neutral category: “Others”.
- Records with null salary values (indicating former employees) were excluded.
- Records with "NULL" departments were also removed from the dataset to ensure departmental-level analysis remains reliable.

