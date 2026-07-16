# PROJECT : Power Bi Project (Mobile_sales_data)

## Project Overview

**Project Title**: Mobile_sales_data_analysis_dashboard
**Database**: Mobile_sales_data

This project is designed to demonstrate Power Bi skills and techniques typically used by data analysts to visualise and analyze mobile sales data. The project involves importing a raw data of mobile saleS  and analysing the yearly data with the help of Power Bi reports & dashboard, performing exploratory data analysis (EDA), and answering specific business questions through this interactive & graphical visualization of data.

##Introduction-
Power Bi is a Microsoft based business intelligence tool that helps in creating graphically summarized interactive reports & dashboards that helps in taking data driven business decisons.

## Objectives

1. **Set up a online mobile sales database**: Import and transform the data in power query editor . The data can be imported from various sources in our case we have imported a Csv file.
2. **Data Cleaning**: Identify and remove any records with missing or null values if any in power query editor itself before loading the dataset.
3. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
4. **Business Analysis**: Use Power Bi  to answer specific business questions and derive insights from the mobile sales data such as creating KPI cards , charts , year to date data analysis etc.

## Project Structure

### 1. Database Import

- **Database Import**: The project starts by downloading raw mobile sales data from kaggle . Importing the Csv file into Power Bi query editor.Transforming the data if required & loading the data for final data visualization.
- **Dashboard Creation**: A page named Overview & Analysis are created to prepare reports & extraxt meaningful data insights. 

### 2. Dashboard Creation

The page structure of dashboard includes 2 pages ie. MTD overview & same period last year. Following below  various indicators are created that are helpful in decision making ----

****KPI cards are categorised into total sales, total quantity, transactions & average price.
****With the help of bar charts the data on the basis of total sales by mobile model are depicted.
****Funnel Chart is prepared which depicts ratings by rating status.
	Ratings are further categorized into using DAX switch true function as mentioned below:
							 *Good 
							 * Poor  
							 *Average 
****Pie charts is created to extract transactions by payment method.Payments methods involves below methods-
							 * UPI
							 * Debit Card
							 * Credit Card
							 * Cash
****Line chart is created to depict the total quantity of sales by monthly basis.
****DAX ie. Digital analytical expression are used in order to arive at year on year revenue workings in form of MTD, QTD & YTD, same period last year, switch true functions etc.
****Table is created to highlight the top brands on the basis of total sales & transactions and another table is created to depict total sales Vs last year data .
**** Several Charts such as column & bar charts are created to depict following data extractions-
							 *Total sales by mobile model
							 *Total sales by city
							 *Total sales & year on year same period last year by year
							 *Total sales & year on year same period last year by quarter
							 *Total sales & year on year same period last year by month
*****Area chart is created in order to visualize total sales by day name.
****Slicers are added in order to filter interactive tables & charts using buttons. Slicers for following are added -
							 * Mobile model
							 * Month wise
							 * Payment Method
							 * Year, Quarter, Month, day 
**** Page navigators are added in order to navigate through different pages seamlessly ie. 
							 * MTD Report
							 * Same Period Last year



-----------END OF THE PROJECT------------

## Findings

- **Customers Demographics**: The dataset includes customers from various cities across entire India actively purchasing different Brand mobiles among their various category of mobile models.
- **Revenue Trends**: There are certain Brands  having particular mobile model such as Iphone, a premium brand having large market share & constant demand among different customers across all regions. 
    Also brands like Xiaomi & vivo are dealing in both affordable & premium category mobiles having a fair amount of market share as well.
- **Brand Insights**: The analysis identifies the brands summarized on basis of mobile models, their frequent order frequency , sales and profit analysis.
- **Mobile Sales revenue- YOY revenue is analysed , with the help of DAX functions data is visualized and compared as Today Vs same period last year.
    Also revenue  trends are distributed among date heirarchy as well.
	
## Reports

- **Customer Summary**: A detailed report summarizing total customers , their cities , their purchasing power & intesrest are evaluated on basis of mobile order frequency & price constarints if any are analysed.
- **Revenue trend  Analysis**: Insights into revenue trend among year, quarter, day & same period lat year.
- **Purchasing Power Analyis**: Customers ratings are evalauted on basis of good, avearge & poor. The status shows how the customer is a KINGPIN in any business & how bad ratings & fewer ratings counts can affet the brand sales in the long run.
- **Brand Market Share**: Reports on top Brands  & mobile models and unique customers served per quantity sold, total revenue earned & total transactions incurred brand wise.

## Conclusion

This project serves as a comprehensive introduction to Power Bi  for data analysts, covering database import, data cleaning, exploratory data analysis, and business-driven visualization techniques. The findings from this project can help drive business decisions by understanding revenue patterns, patients behavior, and doctors, hospitals & insurance provider performance.

