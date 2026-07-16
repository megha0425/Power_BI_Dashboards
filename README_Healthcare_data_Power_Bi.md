# PROJECT : Power Bi Project (Healthcare_data)

## Project Overview

**Project Title**: Healthcare_data_analysis_dashboard
**Database**: Healthcare_data

This project is designed to demonstrate Power Bi skills and techniques typically used by data analysts to visualise and analyze healthcare data. The project involves downloading a raw dataset of healthcare industry from Kaggle and analysing the yearly data with the help pf Power Bi reports & dashboard, performing exploratory data analysis (EDA), and answering specific business questions through this interactive & graphical visualization of data.

##Introduction-
Power Bi is a Microsoft based business intelligence tool that helps in creating graphically summarized interactive reports & dashboards that helps in taking data driven business decisons.

## Objectives

1. **Set up a online Healthcare database**: Import and transform the data in power query editor . The data can be imported from various sources in our case we have imported a Csv file.
2. **Data Cleaning**: Identify and remove any records with missing or null values if any in power query editor itself before loading the dataset.
3. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
4. **Business Analysis**: Use Power Bi  to answer specific business questions and derive insights from the Healthcare data such as creating KPI cards , charts , year to date data analysis etc.

## Project Structure

### 1. Database Import

- **Database Import**: The project starts by downloading the dataset from Kaggle . Importing the Csv file into Power Bi query editor.Transforming the data if required & loading the data for final data visualization.
- **Dashboard Creation**: A page named Overview & Analysis are created to prepare reports & extraxt meaningful data insights. 

### 2. Dashboard Creation

The page structure of dashboard includes 2 pages ie. overview & financial analysis. Following below  various indicators are created that are helpful in decision making ---------

****KPI cards are categorised into Total doctors, total hospitals, total revenue & total number of admissions.
****With the help of bar charts the data on the basis of different patients are categorised.
    The complete data is summarised on the basis of patients -* Patients by Blood Type
							      * Patients by medical condition
							      * Patients by insurance provider
							      * Patients by Medication
****Donut charts are created to extract the patients distribution over various hospitals & among various doctors on the basis of -
							      * Gender Distribution
							      * Admission Type
							      * Test Results
							      * Age Bucket distribution
****Line chart is created to depict the admission trend of patients year on year basis.
****DAX ie. Digital analytical expression are used in order to arive at year on year revenue workings.
****Line & stacked column chart is created in order to calculate top 5 doctors on the basis of revenue generated & patients served.
****Slicers are added in order to filter interactive tables & charts using buttons. Slicers for following are added -
							      * Doctor
							      * Hospitals
							      * Insurance Providers 
**** Page navigators are added in order to navigate through different pages seamlessly ie. overview & financial analysis.



-----------END OF THE PROJECT------------

## Findings

- **Patient Demographics**: The dataset includes patients from various age group such as Teenage, Kids , senior citizen, adults , of different genders male & Female , different blood types & admission types  distributed among various doctors , Hospitals & insurance providers.
- **Revenue Trends**: There are certain hospitals  having particular doctors  serving more patients and generating higher revenue . The list of same is highlighted as top 5 doctors.
- **Patient Insights**: The analysis identifies the patients summarized on basis of blood type, medication , medical condition & insurance providers.
- **Doctors & hospitals YOY revenue- YOY revenue is analysed .
	
## Reports

- **Patients Summary**: A detailed report summarizing total patients across different category.
- **Revenue trend  Analysis**: Insights into revenue trend among hospitals , particular doctors .
- **Doctors , Hospitals & insurance provider Insights**: Reports on top doctors & hospitals and unique patients served per patient. 

## Conclusion

This project serves as a comprehensive introduction to Power Bi  for data analysts, covering database import, data cleaning, exploratory data analysis, and business-driven visualization techniques. The findings from this project can help drive business decisions by understanding revenue patterns, patients behavior, and doctors, hospitals & insurance provider performance.

