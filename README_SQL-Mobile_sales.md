# PROJECT : SQL PROJECT (Mobile_sales_analysis)
## Project Overview

**Project Title**: Mobile_sales_analysis
**Database**: Mobile_sales_db

This project is designed to demonstrate SQL skills and techniques typically used by data analysts to explore, clean, and analyze retail sales data. The project involves setting up a retail sales database, performing exploratory data analysis (EDA), and answering specific business questions through SQL queries. This project is ideal for those who are starting their journey in data analysis and want to build a solid foundation in SQL.

## Objectives

1. **Set up a online book  sales database**: Create and populate a books sales database with the provided sales data, ordered data & customer data.
2. **Data Cleaning**: Identify and remove any records with missing or null values.
3. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
4. **Business Analysis**: Use SQL to answer specific business questions and derive insights from the sales data.

## Project Structure

### 1. Database Setup

- **Database Creation**: The project starts by creating a database named `Mobile_sales_db`.
- **Table Creation**: A table named `retail_sales` is created to store the sales data. The table structure includes columns for transaction ID, sale date, sale time, customer ID, gender, age, product category, quantity sold, price per unit, cost of goods sold (COGS), and total sale amount.
----- Create Database Mobile_sales_db
Create Database Mobile_sale_db;

----Create Table Mobile_Sales
Drop Table if exists Mobile_sales;

Create Table Mobile_Sales(
	Transaction_id Serial Primary key,
     Order_date date,
     Day_name Varchar(10) ,
     Brand Varchar(50),
     Units_sold Integer,
     Price_per_unit Numeric(8,2),
     Customer_name Varchar(80),
     Customer_age Integer,
     City Varchar(50),
     Payment_method Varchar(20),
     Customer_ratings Integer,
     Mobile_model Varchar(100)
     );
     
     Select * From mobile_sales;


### 2. Data Exploration & Cleaning

- **Record Count**: Determine the total number of records in the dataset.
- **Customer_id Count**: Find out how many unique customers are in the dataset.
- **Genre Count**: Identify all unique product categories in the dataset.
- **Null Value Check**: Check for any null values in the dataset and delete records with missing data.

```sql
SELECT COUNT(*) FROM Units_sold ;
SELECT COUNT(City) FROM Mobile_sales;
SELECT DISTINCT Customer_name FROM Mobile_sales;

SELECT * FROM Mobile_sales
WHERE 
    Order_date IS NULL OR Customer_name IS NULL OR City IS NULL OR 
    Cusrtomers_age IS NULL OR Customer_ratings IS NULL OR Units_sold IS NULL  ;


```
-----Following below are data retreived using SQl queries to give meaningful insights:
     
     Q1: Find the total units sold of mobile Galaxy Note 20
      Select 
      Sum(Units_sold) as Units_sold_Galaxy_note_20
       From mobile_sales
      Where mobile_model = 'Galaxy Note 20';
      
      Q2: Find the total units sold of each mobile model as highest sales to lowest
      Select Mobile_model,
      Sum(Units_sold) AS Units_sold
      From Mobile_sales
      Group By Mobile_model
      Order By units_sold Desc;
     
     Q3: Find the  lowest 5 total units sold of mobile model among all 
     Select Mobile_model,
      Sum(Units_sold) AS Units_sold
      From Mobile_sales
      Group By Mobile_model
      Order By Units_sold Asc
      Limit 5;
      
      Q3: Find the  Total Sales of each Brand as per their mobile model
      Select Brand, mobile_model,
      Sum(Units_sold * Price_per_unit) As Total_sales
      From Mobile_sales
      Group By Brand, mobile_model
      Order by Total_sales Desc;
      
      Q5: Find Total Sales of all Brands
	Select
    Sum(Units_sold * Price_per_unit) As Total_sales
    From Mobile_sales;
    
    Q6: Find the total qty sold of Apple Iphone 12 and total sales
    Select  
    Sum(Units_sold * Price_per_unit) As Apple_iphone12_sales
    From Mobile_sales
    where Brand='Apple' And Mobile_model='iPhone 12';
    
    Q7: Find the top 10 customers on basis of purchase made
    Select Customer_name,
	Sum(Units_sold * Price_per_unit) As Total_Purchase
    From mobile_sales
    Group By Customer_name
    Order By Total_purchase Desc 
    Limit 10;
    
    Q7: Find the city with Purchase wise data
    Select City,
	Sum(Units_sold * Price_per_unit) As Total_Purchase
    From mobile_sales
    Group By City
    Order By Total_purchase Desc
    
    Q9: categorise the total purchase by payment methods
    Select Payment_method,
	Sum(Units_sold * Price_per_unit) As Total_Purchase
    From mobile_sales
    Group By payment_method 
    Order by payment_method desc;
    
    Q10; Find the day on which most number of units are sold
    Select Day_name,
    Count(units_sold) as Units_sold
    From mobile_sales
    Group By Day_name
    Order By units_sold desc
    Limit 1;
    
    Q11. Find the product with  top 8 highest number of ratings count
    Select Brand, Mobile_model,
    Count(Customer_ratings) as Ratings_count
    From mobile_sales
    Group By Brand, Mobile_model
    Order By Ratings_count,Brand, Mobile_model desc
    Limit 8;
    
    Q12: Categorise the customer age into , Children,Teenagers, Young Adults , Adults, Senior Citizen. Find total Purchsaes by each category
    Select  
    Case 
    when customer_age <13 then 'Children'
    when customer_age Between 13 and 19  Then'Teenagers'
    when customer_age between 20 and 35  then 'Young Adults'
	when customer_age between 36 and 60 then 'Adults'
	Else 'Senior Citizens' 
    End as age_group,
    
    Sum(Units_sold * Price_per_unit) as Total_purchases
    From mobile_sales
    Group By age_group
    Order by Total_purchases Desc;
    
    Q13. Find the age_group category wise, brand & city wise total sales  distribution summary . Top 10
    Select  
    Case 
    when customer_age <13 then 'Children'
    when customer_age Between 13 and 19  Then'Teenagers'
    when customer_age between 20 and 35  then 'Young Adults'
	when customer_age between 36 and 60 then 'Adults'
	Else 'Senior Citizens' 
    End as age_group,
    city,
    Brand,
    count(customer_age) as Customers_count,
    Sum(units_sold) as Total_units_sold,
    Sum(Units_sold * price_per_unit) as Total_purchase
    
    From mobile_sales
    Group By age_group , city,Brand
    Order by Total_purchase desc, age_group , city, Brand
    limit 10
    ;
    
    Q14. Calculate year wise total_sales
    Select 
    Date_format(Order_date,'%Y') as Sales_year,
    Sum(units_sold * Price_per_unit) as Total_sales
    From mobile_sales
    Group By Sales_year;
    
    Q15. Calculate the week with highest sales in the year 2023
    Select 
    Week(Order_date) as Week_number,
     Sum(units_sold * Price_per_unit) as Total_sales
     From mobile_sales
     Where date_format(Order_date,'%Y') = '2023'
     Group By Week_number
     Order By Total_sales Desc
     Limit 1 ;
     
     Q16. Calculate the month  with lowest customer ratings in Year 2022. Top 3
     Select 
    Month(Order_date) as Month_2022,
     Count(Customer_ratings) as Ratings_count
     From mobile_sales
     Where date_format(Order_date,'%Y') = '2022'
     Group By Month_2022
     Order by Ratings_count asc
     Limit 3 ;

	Q17. Calculate Day wise sales made in year 2021
	Select 
	 Day_name,
	Sum(units_sold * Price_per_unit) as Total_sales
	From Mobile_sales
	Where Date_format(Order_date,'%Y') ='2021'
	Group By Day_name;
    
    Q18. Categorise the customer ratings status as per mobile model
    Select  
    Mobile_model,
    Case 
    when customer_ratings >=4 then 'Good'
    when customer_ratings >2  Then'Average'
	Else 'Poor' 
    End as Ratings_status,
    Count(Customer_ratings) as Ratings_count
    From mobile_sales
    Group By Ratings_status, Mobile_model
    Order By Ratings_count DEsc;
    
    Q19. Count the total customer ratings and categorise as per their status
    Select 
    Case 
    when customer_ratings >=4 then 'Good'
    when customer_ratings >2  Then'Average'
	Else 'Poor' 
    End as Ratings_status,
    Count(Customer_ratings) as Ratings_count
	From Mobile_sales
	Group by Ratings_status;
    
	Q20.Calculate the ratings count of Xiaomi brand in year 2023 as per the category
    Select Brand,
    Count(Customer_ratings) as Ratings_count,
    Case 
    when customer_ratings >=4 then 'Good'
    when customer_ratings >2  Then'Average'
	Else 'Poor'
    End as Ratings_status
    From Mobile_sales  
    Where Brand ='Xiaomi' and 
    Date_format(Order_date,'%Y') = '2023'
    Group By Brand , Ratings_status
    Order By Ratings_count Desc;

### 3. Data Analysis & Findings

-----------END OF THE PROJECT------------

## Findings

- **Customer Demographics**: The dataset includes customers from various cities, with units sold  sales distributed across different countries having different brands among different mobile models such as Iphone, Samsung, Xiaomi etc.
- **High-Value Transactions**: Several transactions had a total sale amount greater than 50,000 Rs., indicating premium purchases on mobiles purchased within certain cities, among different age group of customers ranging among Teenagers, Adult, Young adults.
- **Sales Trends**: There are certain mobiles  from particular brands having ordered count more than 4 indicating high demand for those mobile models such as Vivo with price range 10,000-25,000, and premium phones such as Samsung and Apple ranging above 50,000.
- **Customer Insights**: The analysis identifies the top-spending customers and the most popular mobile models based on average customer ratings .
	The customer ratings  are categorised as Good , average and poor.
-** Units sold and Inventory Verification **: The analysis identifies units those having larger demands indicating those models needs to be reodered frequently to cope up with the demand.

## Reports

- **Sales Summary**: A detailed report summarizing total units sales, customer demographics, and category wise Brands & their mobile models performances.
- **Trend Analysis**: Insights into sales trends cities for particular mobile model, Brand or price range.
- **Customer Insights**: Reports on top customers and unique customer counts per category. The customer ratings gave us a fair view on how the different models are performing and what needed attention.

## Conclusion

This project serves as a comprehensive introduction to SQL for data analysts, covering database setup, data cleaning, exploratory data analysis, and business-driven SQL queries. The findings from this project can help drive business decisions by understanding sales patterns, customer behavior, and product performance.

