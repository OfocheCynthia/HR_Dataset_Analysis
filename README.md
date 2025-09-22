# HR_Dataset_Analysis
## Overview:

+ This is an employee dataset analysis report for a company 

___

## Contents

+ [Project Overview](#Project-Overview) |+ [Data Source](#Data-Source) |+ [Tools Used](#Tools-Used) |+ [Table Outlay](#Table-Outlay) |+ [Query Language](#Query-Language) |+ [VIsualisation](#VIsualisation)

---
## Project Overview

>> This project analyzes an HR dataset containing employee information such as age, gender, department, grade, salary, tenure, hire date, and location. The aim was to perform end-to-end data analysis using:
+ Excel → Data cleaning and preprocessing.
+ SQL → Querying and extracting workforce insights.
+ Power BI → Interactive dashboards and visualization.
+ This project showcases how HR data can be transformed into actionable insights to support decision-making in areas like employee retention, compensation, and workforce planning.

--- 
## Data Source
www.kaggle.com/dataset

---
## Tools Used
+ Pivot table/ Charts
+ PowerBi
+ SQL

## Table Outlay:
FIrst Four Rows

|Gender|	HireDate|	Date of Birth|	Today's date|	Age| Tenure|	Location|	Department|	Job Grade|
|---|---|---|---|---|---|---|---|---|
|M|	7/31/2002|	4/11/1982|	9/21/2025|	43|	23|	Abuja|	Sales|	Officer|
|M|	2/26/2010|	4/5/1978|	9/21/2025|	47|	15|	Lagos|	Sales|	Officer|
|M|	12/12/2007|	6/10/1974|	9/21/2025|	51|	17|	Lagos|	Production|	Officer|

## Query Language:

### SQL
Some of the query languages to retrieve records are displayed here

```SQL
---Employees Age group Segementation---
SELECT Employee_ID, Age,
CASE
WHEN Age <= 30 THEN 'Youth'
WHEN Age >= 40 THEN 'Adult'
ELSE 'Elders'
END AS Employee_AgeGroup
FROM Company_Dataset;

````

```SQL
---Retrieve the lonest serving employees---
SELECT TOP 10 * FROM Company_Dataset
ORDER BY Tenure DESC;

```

```SQL
---Retrieve Employee distribution by department---
SELECT Department, 
COUNT(*) AS Totalemployees
FROM Company_Dataset
GROUP BY Department
ORDER BY Totalemployees DESC;

```

```SQL
---Retrieve the total employee in the company---
SELECT COUNT(*)AS TotalEmployees
FROM Company_Dataset;

```

```SQL
---Retrieve total employee in different location---
SELECT Location, 
COUNT(*) AS Totalemployees
FROM Company_Dataset
GROUP BY Location
ORDER BY Totalemployees DESC;

```

## Visualisation
### Pivot Tables

<img width="1150" height="397" alt="Company Data Pivot table" src="https://github.com/user-attachments/assets/14333d11-524f-4c55-b187-b285b095f685" />

### Dashboard

<img width="1204" height="436" alt="Company Dashboard" src="https://github.com/user-attachments/assets/fd2fd92b-d2ff-40b8-9ffd-48f7ac7c3b11" />

### Link to Charts
[Link to Chart]

[View my Linkedin](https://www.linkedin.com/in/ofochecynthia)
