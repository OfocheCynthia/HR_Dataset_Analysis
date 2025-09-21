# HR_Dataset_Analysis
## Overview:

+ This is an employee dataset analysis report for a company 

___

## Contents

+ [Project Overview](#Project-Overview) | + [Data Source](#Data-Source) | + [Tools Used](#Tools-Used) | + [Table Outlay](#Table-Outlay) | + [Query Language](#Query-Language) | + [VIsualisation](#VIsualisation)

---
## Project Overview

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

```
---Retrieve Employee distribution by department---
SELECT Department, 
COUNT(*) AS Totalemployees
FROM Company_Dataset
GROUP BY Department
ORDER BY Totalemployees DESC;

---Retrieve the total employee in the company---
SELECT COUNT(*)AS TotalEmployees
FROM Company_Dataset;

---Retrieve total employee in different location---
SELECT Location, 
COUNT(*) AS Totalemployees
FROM Company_Dataset
GROUP BY Location
ORDER BY Totalemployees DESC;
