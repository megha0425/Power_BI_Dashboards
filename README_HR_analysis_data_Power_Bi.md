# PROJECT : Power Bi Project (HR_analysis_data)

## Project Overview

**Project Title**: Human_Resource_data_analytics_dashboard
**Database**: Human_resource_data

This project is designed to demonstrate Power Bi skills and techniques typically used by data analysts to visualise and analyze human resource data. The project involves downloading a raw dataset of hr industry from Kaggle and analysing the yearly data with the help of Power Bi reports & dashboard, performing exploratory data analysis (EDA), and answering specific business questions through this interactive & graphical visualization of data.

##Introduction-
Power Bi is a Microsoft based business intelligence tool that helps in creating graphically summarized interactive reports & dashboards that helps in taking data driven business decisons.

## Objectives

1. **Set up a online Human Resource database**: Import and transform the data in power query editor . The data can be imported from various sources in our case we have imported a Csv file.
2. **Data Cleaning**: Identify and remove any records with missing or null values if any in power query editor itself before loading the dataset.
3. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
4. **Business Analysis**: Use Power Bi  to answer specific business questions and derive insights from the Human resource data such as creating KPI cards , charts , year to date data analysis etc.

## Project Structure

### 1. Database Import

- **Database Import**: The project starts by downloading the dataset from Kaggle . Importing the Csv file into Power Bi query editor.Transforming the data if required & loading the data for final data visualization.
- **Dashboard Creation**: A page named Overview &  Finacial Analysis are created to prepare reports & extraxt meaningful data insights. 

### 2. Dashboard Creation

The page structure of dashboard includes 2 pages ie. Attrition overview & attrition driver & insights. Following below  various indicators are created that are helpful in decision making ---------

****KPI cards are categorised into Total Employees, Average monthly salary, average tenure , average % salary hike & attrition rate.

****With the help of bar charts  & donut chart ,the data on the basis of different employees are categorised on basis of attrition rate.
    The complete data is summarised on the basis of employees * By salary slab
							      * By overtime
							      * By Job Level

****Bar, column charts  & donut chart are created to extract the employees who are leaving the organization due to -
							      * By Age group
							      * By Gender
							      * By Martial Status

****Bar , column charts  & donut chart are created to extract the employees who are leaving are leaving from where ?
							      * By Job Role
							      * By Department

**** Charts are created to depict the impact on employees due to career growth & tenure-
							      * Tenure Vs Attrtition
							      * Promotion gap Vs Attrtition

****DAX ie. Digital analytical expression are used in order to arive at year on year employees attrition rate & average salary data.

****Insights are added in order the workings such as Single employees btw 18-25 shows highest attrition. Males change their job more frequently than females.
****Slicers are added in order to filter interactive tables & charts using buttons. Slicers for following are added -
							      * Job Roles
							      * Department

**** Page navigators are added in order to navigate through different pages seamlessly ie. Attrition overview & attrition driver & insights.



-----------END OF THE PROJECT------------

## Findings

- **Employees Demographics**: The dataset includes employees from various age groups , gender based distribution and martial status based data distributed.

- **Attrition Trends**: There are certain departments from where attrition rate is higher than average rate of attrition due to salary constraints or work environment.

- **Job roles Insights**: The analysis identifies the job roles where salary is low and promotions have not done lately the major reason of why employees are leaving .

	
## Reports

- **Employee Summary**: A detailed report summarizing total employees across different department on different job roles.

- **Attrition trend  Analysis**: Insights into attrition  trend due to factors like age, gender, martial status , department, salary , working environment etc.


## Conclusion

This project serves as a comprehensive introduction to Power Bi  for data analysts, covering database import, data cleaning, exploratory data analysis, and business-driven visualization techniques. The findings from this project can help drive business decisions by understanding attrition patterns, employees behavior, and various departments working environment & performance.

