# DSA-DATA-ANALYSIS-CAPSTONE-PROJECT-PALMORIA-GROUP
This Power BI dashboard delivers an in-depth HR Analysis for Palmoria Group, which reveals gender, salary, and performance disparities across regions amid public scrutiny, guiding leadership on equity and compliance improvements.

## Case Study 2: Palmoria Group HR Review Analysis 

### Project Overview
This Data Analysis project showcases a comprehensive HR analytics case study conducted for Palmoria Group, a Nigerian manufacturing company under public scrutiny for gender imbalance and compensation disparities within its workforce. Sparked by a damaging media headline “Palmoria, the Manufacturing Patriarchy” the company’s leadership initiated a strategic push toward equity and transparency.
As the HR Analytics Lead, I conducted a detailed, data-driven investigation into critical HR issues across three regional locations, focusing on:
 - Gender distribution and workforce diversity.
 - Salary structure and pay equity.
 -  Employee performance metrics.
 - Regulatory and compliance alignment.

The project aims to drive accountability, foster workplace inclusivity, and guide Palmoria Group toward sustainable HR practices.

### Dataset Used
The primary sources of data used here is Palmoria  Group emp-data.csv and Palmoria Group Bonus Rules.xlsx and this is an open source data that can be freely downloaded from an open source online such as Kaggle or FRED or any other data repository site.

### Tools Used:
- Power BI Desktop for data modeling and visualization.
- Power Query Editor for cleaning and transformation.
- DAX for calculated measures.
- Excel for supplementary bonus rule data.

### Process : Data Cleaning & Preparation
Before analysis, the HR datasets were explored using ETL process - Extract, Transform and Load :
- Employees who refused to disclose their gender were classified under a neutral category: “Others”.
- Records with null salary values (indicating former employees) were excluded.
- Records with "NULL" departments were also removed from the dataset to ensure departmental-level analysis remains reliable.

### Questions & Dashboard Insights
 1. Gender Distribution Analysis:
Bar chart shows visual breakdown of gender representation company-wide by region and departments.
Identification of male-dominated and female-dominated departments.
Pie chart shows Insight into regions with the widest gender disparity.

 2. Ratings insights based on Gender:
Histogram showing Rating Distribution by Gender.
Boxplots visuals to highlight disparities in performance evaluations.
Identification of bias-prone departments.

 3. Salary Structure & Gender Pay Gap Analysis
Scatter plot visuals showing where salary discrepancies are most pronounced among gender.
Bar chart shows evaluation of Average salary by gender, region and department.
Identification of potential gender pay gaps.

 4. Compliance with Salary Regulation
A recent law requires a minimum annual salary of $90,000.
Histogram showing salary bands in $10,000 intervals (e.g. $10k–$20k, $20k–$30k, etc.).
Bar chart showing Employee falling below minimum salary threshold by department and region.

 5. Annual Bonus Allocation Based on Performance
Bonus rules applied using an external rating-bonus mapping file.
Each employee’s bonus amount calculated based on performance.
Total Amount to be paid to individual employee = Salary +  Bonus Amount calculated.
Bar chart shows Total bonus payout company-wide.
Table showing Individual Employee Bonus Payments.

### Exploratory Data Analysis
Using Calculated measures, the following Dax expressions were used during the analysis:
- Gender Count = COUNT('Employee'[Gender])
- Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))
- Average Rating by Gender = AVERAGE('Employee'[Rating])
- Rating Count by Gender = COUNT('Employee'[Rating])
- Average Salary by Gender = AVERAGE('Employee'[Salary])
- Salary Count by Department and Region = COUNT('Employee'[Salary])
- Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])
- Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)
- Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'
  
### Dasboard  
https://github.com/Abee-Udoh/DSA-DATA-ANALYSIS-CAPSTONE-PROJECT-PALMORIA-GROUP/blob/main/Palmora_Group_clean%202.pbix  

### Project Insights & Recommendations
- Management should investigate gender imbalance in Regions and Department.
- Evidence suggests a gender pay gap in certain departments;recommend salary audits.
- A portion of employees earn below the mandated $90,000 minimum;urgent adjustment required.
- Bonus distribution reflects fair alignment with performance; however, further scrutiny of rating practices is advised.

### Conclusion
 This analysis highlights key gender disparities in Palmoria’s workforce, including uneven gender distribution, pay gaps, and performance rating inconsistencies. It also reveals non-compliance with the $90,000 minimum wage regulation in some areas. Addressing these issues through fair pay reviews, inclusive hiring, and improved performance evaluations will position Palmoria for sustainable growth and global expansion.


