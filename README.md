# LITA_PROJECTS

## PROJECT TITLE: LITA DOCUMENTATIONS 
### Project Outlines
---
[PROJECT OVERVIEW](#project-overview)

[DATA SOURCE](#data-source)

[TOOL USED](#tool-used)

[DATA CLEANING AND PREPARATION](#data-cleaning-and-preparation)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)

[DATA VISUALIZATION](#data-visualization)

---
### PROJECT OVERVIEW

The purpose of this project is to documentation some of my works in LITA classes so as to serve as a future reference to other works I will be doing. This documentation consist of some calculations in excel classes, queries for SQL classes and some visual done in power Bi classes.

### Data source
The data used for this analysis was sent to the students from our instructor through telegram and individual LMS canvas account. Some of the data set used include
- Excel [Donwload Here](https://www.microsoft.com/en-ng/search/explore?q=Microsoft+Excel+2016+download)
  - Excel Function 1.xlsx (Number)
  - Excel Function 2.xlsl (Text)
  - Excel Function 3.xlsl (Lookup)
  - Pivot Table.xlsx (IF function)
  
- SQL [Download Here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) for the studio [Download Here](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)
  - LITA_DB Query.txt
  - SQL queries for 19&20.txt
  - SQL queries for 24.txt
  - International Breweries.csv etc
  
- Power BI [Download Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
  - Loan Data.xlsx
  - HR Data.xlsx
  - Columnar data.xlsx
  - Excel Function 2.xlsx (Text)
  - Pivot table.xlsx etc

### Tool used  
- Microsoft Excel- This tool was used to clean the dataset, enter data using form, perform some caculations using formulas and functions as well as summaries the data using pivot table etc.
  
- SQL Server Management Studio-for querying of the dataset, make use of different commands such as Clauses (Having, Group and order), Join (Inner, Left, Right, Full outer joins), Range operator (between, not between), Union operator and Union all, SQL aggregates (sum, average, count, max, min), case when, view etc.
  
- Power BI- under this tool we made used of power querry to clean the data (remove some blank rows and columns, append row and merge columns), perform some data analysis expressin (DAX) functions using concatenate, trim, change text to upper, proper and lower case, create measure and calculated column, create dashboard to visualise some  insights etc.
  
- GitHub- this is used to build my portfolio as well as document most of what we were taught in the class

### Data cleaning and Preparation
After opening the dataset, we perform some data cleaning such as
- Data formatting
- Add another columns, pages to the dataset
- Removing some null columns and rows in the dataset
- Perform some calculation using the excel funtions, SQL aggregates and DAX function
- Perform some visuals using pivot table and power BI etc

### Exploratory Data Analysis 
I provide answer to some questions on the dataset such as 
- Get the total sum of, average of employee sallary as well as count number of employees in all states
- Change text to upper, lower and proper case
- Find basic salary of some employees as well as other incentives paid to them such as transport, health, housing, gross allowances 

### Data analysis
These are some of the code and queries used to achieve our analysis
```Excel
=SUM(D8:D27)
=MIN(D8:D27)
=AVERAGE(D8:D27)
=COUNTA(B8:B27)
=SUMIF(C8:C27,C9,D8:D27)
=AVERAGEIF(C8:C27,C16,D8:D27)
=RIGHT(B10,4)
=MID(B10,3,6)
=UPPER(E6)
=PROPER(TRIM(B7))
=C6&$E$4
=C6&D6&$E$4
=B9&" "&C9
=VLOOKUP(E9,'Simple Salary Structure'!$B$8:$I$16,2,FALSE)
=IF(J30778<=20,"Low",IF(J30778<=50,"Medium","High"))
```
``` SQL
CREATE TABLE EMPLOYEE (
staffid varchar (10) not null,
firstname varchar (255) not null,
secondname varchar (255) not null,
Gender varchar (10),
Date_of_birth date,
Hiredate datetime,
Primary Key (staffid)
)

select * from employee

select sum(salary) as Total_Salary from salary

update salary
set salary=7056999.9994
where staffid= 'AB401'

select count(*) from Payment
where Payment_Method= 'Transfer'

select count(staffid) as StaffperState, state_of_origin from Employee
Group by state_of_origin
Order by 2 desc

select * from salary
where salary>=100560.934
```
These are some of the screenshots of the my works

![Excel Function 1](https://github.com/user-attachments/assets/958737a3-a793-464d-a1d6-14dd3c2baaf9)

![Function 2 cleaning 1](https://github.com/user-attachments/assets/e8ae6e4e-8997-4d3f-88d9-d4d9233c3f6c)

![Function 2 extraction](https://github.com/user-attachments/assets/d1c47272-6276-4c8c-8e51-f887782a7b5c)

![Vlook up](https://github.com/user-attachments/assets/0a760bf1-5432-4ff5-b90c-e531d9f5530f)

![IF function](https://github.com/user-attachments/assets/552bd6b5-dcbf-4df2-9c3d-d9918419cf46)

![Pivot table Class](https://github.com/user-attachments/assets/b6b09dc2-b754-403d-b38c-3504c7ae1ef5)

![CHART 1](https://github.com/user-attachments/assets/387f188e-ae4f-4600-bbfc-37078e5b322f)

![CHART 2](https://github.com/user-attachments/assets/420e97c4-fd94-4fbe-9f87-c9c9c2dc2819)

![SQL 1](https://github.com/user-attachments/assets/5d700147-64f0-4f46-9c0f-7a1474aa7141)

![SQL 2](https://github.com/user-attachments/assets/15aece22-c2d5-4eb7-b28c-dbc4d1ba9bd5)

![SQL 3](https://github.com/user-attachments/assets/c4bfc1f2-ec08-4769-bbf1-104aaaabee99)

![SQL 4](https://github.com/user-attachments/assets/4e0a1af6-766e-4c08-ab5d-3a3cd9a6a789)

![SQL 6](https://github.com/user-attachments/assets/ab29d691-b973-4ed8-8029-995193621a36)

![SQL 7](https://github.com/user-attachments/assets/22c05514-6a63-4569-848d-bf27de82333d)

![SQL VIEW 8](https://github.com/user-attachments/assets/a6fdb836-088a-4866-aaeb-d7cd347e8a1f)

![DASHBOARD 1](https://github.com/user-attachments/assets/f65cfd30-9e7d-477d-9ff2-2da7efbaec18)

![DASHBOARD 3](https://github.com/user-attachments/assets/5dc5a7bb-c880-414c-8f26-d4a44fd7cc30)

![DASHBOARD 4](https://github.com/user-attachments/assets/85d79ff8-8d9e-4d97-9847-04057bb885d8)

![DASHBOARD 5](https://github.com/user-attachments/assets/114ce559-8f75-4b36-b5ca-5e7b0c0be6c5)

![MAP](https://github.com/user-attachments/assets/a6902e9c-18fc-46d2-b7bf-ef0cffa6bcd0)









