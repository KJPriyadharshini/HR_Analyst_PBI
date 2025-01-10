

# HR Analytics-Dashboard

## Problem Statement


This dashboard helps the HR management understand their employees. It helps the them know their employees attrition with respect to age, salary, job role, work experience at the company and their educational qualification. Through different visualizations, they get to analyze their employees attrition rate and improve their job satisfaction by identifying the problem area. It also lets them know the attrition rate, thus by using this dashboard they can further work on areas of improvement.


Since, the job satisfaction of Lab Technicians and Sales Excecutive are very low, they must work on improving their policies.


Also since attrition rate is very high where salary of employees is below 5k, they must try to update it.




### Steps followed 


- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : It was observed that in none of the columns errors & empty values were present except column named "WorkLifeBalance".
- Step 4 : The "WorkLifeBalance" column was sorted and the top rows that contained null value was removed.
- Step 5 : Duplicate values where identified in the "EmpID" column by grouping it by counting the number of rows.
- Step 6 : Every column in the table was selected and right clicked to remove duplicates.
- Step 7 : It was observed that the column "BusinessTravel" has different values that repeats itself. The values where were replaced by right clicking the column name.
- Step 8 : A conditional column called "Attrition_Count" was created in which, 'yes and no' values where changed to boolean using if else condition.
- Step 9 : In the report view, canvas was customised by changing the canvas settings in visualizations.
- Step 10 : In order to represent KPIs, the card visual was added using card icon in the visualizations pane in report view. 
- Step 11 : The card visual was added for count of employees, attrition, attrition rate, avg salary, avg age, avg years at company.
- Step 12 : The attrition rate was a measure calculated using DAX formula,
           
           AttritionRate = SUM(HR_Analytics[Attrition_Count])/SUM(HR_Analytics[EmployeeCount])
- Step 13 : A bar chart was also added to the report design area representing the count of attrition. While creating this visual, field named "Age" was also added to the Legends bucket, thus count of attrition are also segregated according the age. 
- Step 14 : A Donut chart was used to represent attrition with respect to different educational background mentioned below,


  (a) Life Sciences


  (b) Medical
  
  (c) Marketing
  
  (d) Technical Degree
  
  (e) Others
- Step 15 : Two other horizontal stacked bar chart was added to the report where X axis represented count of attrition and Y axis represented salary and job role.
- Step 16 : A filter was added to the "Attrition by Job Role" where TOP N (4) basic filter was applied.

- Step 17 : An area chart was included in the dashboard where Years At Company represented X axis and count of attrition represented Y axis.
- Step 18: Advance filter for the line chart is applied for years less than 12 years.
Snap of the advance filter,

- Step 19 : A Matrix was added to represent the job satisfaction of the different employees in different job roles.
- Step 20 : In the report view, under the insert tab, a text box was added to the canvas, where name of the dashboard is added.
- Step 21 : The slicer is added to the report view in tile format. The values are filtered by department.

Snap of the slicer,
- Step 22 : A tree chart was added to the report view to show the count of attrition by the genders.

- Step 23 : The report was then published to power BI service.

# Report Snapshot (Power BI DESKTOP)

![image](https://github.com/user-attachments/assets/7b537da0-f198-4469-b6c9-3fb8545027cc)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.


Following inferences can be drawn from the dashboard;


### [1] Total Number of Employees = 1470


   Attrition value = 237


   Attrition rate = 16.1%


   Average age of employees = 37

        Attrition rate is more where employees age is between 26 and 35.


   Average years worked at company = 7 Years

        Attrition rate is high during the first five years at company.


   Average salary of employees = 6.5K

        Attrition rate is high where the salary of employee is less than the average salary.           
           
These values will change if different visual filters will be applied.  
  


 ### [2] Some other insights
 
 ### Attrition w.r.t Job role & satisfaction
 
 a) Employees with life science and medicinal background have more attrition rate than the others.

 b) The job satisfaction of Lab Technicians, Sales Excecutive and Research Scientists are very low resulting in high attrition rate. 

# HR_Analytics-Dashboard.md.txt
Displaying #HR_Analytics-Dashboard.md.txt.
