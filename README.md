#Project: HR Analytics Dashboard using Power BI

Objective: Designed and developed an interactive HR Analytics Dashboard to analyze employee data and identify trends within the organization.

#Tools and Technologies Used:

Power BI: Leveraged Power BI for data visualization and business intelligence.
Microsoft Excel: Prepared and cleaned the raw data before importing it into Power BI.

#The Objective of the HR Dashboard | Business Problem |Business Requirement :
 

Composition of the Workforce: Understand the composition of the workforce by department, education field, business travel frequency, gender, job role, and age group.
HR KPIs: Analyze employee count, average salary, average monthly salary, average age, average salary hike, average Job satisfaction score, and gender ratio.
Identify trends and patterns in employee data across different parameters like Education, Age group, and Department.
Analyze different HR KPIs for different Job roles.
Show the impact of Age & Department on Salary.
Employee Attrition Analysis: Identify the factors that influence employee turnover and retention, such as salary, age, gender, education, and employee demographics (e.g., age, marital status, work-life balance).
Gain insights into areas with high attrition rates to inform targeted retention strategies.
Analyze the attrition rate by various parameters including business travel, job satisfaction, marital status, work-life balance, monthly income, and age.
Compare the attrition rates in different departments such as Sales, R&D, and HR.


#Key Features:

Created visualizations for employee demographics, attrition rates, and salary distribution.
Implemented filters to allow dynamic exploration of data by different dimensions (e.g., age, gender, education).
Developed custom measures to calculate attrition rates and average salary.
Collaborated with HR stakeholders to understand their requirements and iteratively improve the dashboard.

#Here are some of the things that we can do to explore and understand the data:

Check the number of rows and columns in the data set and their names and data types.
Check the range, mean, median, mode, standard deviation, and distribution of the numerical variables, such as age, salary, satisfaction, etc.
Check the frequency, percentage, and proportion of the categorical variables, such as gender, department, job role, attrition, etc.
Check for any missing, invalid, or inconsistent values in the data set and handle them appropriately.
Check for any outliers or anomalies in the data set and decide whether to keep them or remove them.
Check for any correlations or relationships between the variables and visualize them using charts or graphs.


#DAX Measures for HR Dashboard :

//Measure to Calculate Attrition Count
Attrition Count = CALCULATE([Employee Count], HR_Analytics[Attrition]="Yes")
//Measures to Calculate Attrition Rate
DIVIDE ([Attrition Count],CALCULATE ( [Employee Count], ALL ( HR_Analytics[Attrition] ) ),0)
Learn More About Calculate & Divide DAX Power BI Functions.

//Measures for attrition Target
Attrition Target = 0.2

//Measures to calculate Average Age
Average Age = AVERAGE(HR_Analytics[Age])

//Measures to calculate Average Job Satisfaction
Average Job Satisfaction = AVERAGE(HR_Analytics[JobSatisfaction])

//Measures to calculate Average Monthly Salary
Average Salary = [Monthly Salary]/[Employee Count]

//Measures to calculate Average Salary Hike
Average Salary Hike = AVERAGE(HR_Analytics[PercentSalaryHike])

//Measures to calculate Average Yaers at Company
Average Years = AVERAGE(HR_Analytics[YearsAtCompany])

//Measures to calculate Employee Count
Employee Count = DISTINCTCOUNT(HR_Analytics[EmpID])

//Measures to calculate Gender Ratio

Gender Ratio =
DIVIDE (
    CALCULATE ( [Employee Count], HR_Analytics[Gender] = "Female" ),
    CALCULATE ( [Employee Count], HR_Analytics[Gender] = "Male" ),
    0
)

//Measures to calculate Monthly Salary
Monthly Salary = SUM(HR_Analytics[MonthlyIncome])


#Impact:

Empowered HR teams to make data-driven decisions related to workforce management.
Identified areas for improvement, such as attrition hotspots and salary disparities.
Received positive feedback from management for the clarity and usability of the dashboard.

#Skills Demonstrated:

Data visualization
Business intelligence
Data cleaning and transformation
Stakeholder collaboration

![HR Analytics Project](https://github.com/BiswojitMohanty/Insurance-Data-Analysis/assets/155844093/ed80301e-e34f-4dc1-af58-05f58c158365)
