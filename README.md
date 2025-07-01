# DSA-project-2-Documentation

## Project Topic - kultra Mega Stores Inventory 

### Project Overview

The Kultra Mega Stores Inventory project aims to analyze sales data from 2009 to 2012 to gain insights into product performance, customer behavior, and operational efficiency. The analysis will focus on identifying trends, patterns, and correlations in the data to inform business decisions.

### Data source 

The primary source of data uesd here is data inventory and this is an open source data that can be freely downloaded from open source online such as kaggle or any other repository site.

### Tools Used 

-  SQL ( for quering and data slicing
-  Microsoft excel( for cleaning
-  Power BI( for visual analytic and dashboard
-  GitHub ( version control and hosting

### Data Cleaning and Preparation 
In the initial phase of the data cleaning and preparation, l perform the following actions 
1. Data loading and inspection
2. Handling mising variables
3. Data cleaning and formatting

### Data Analysis 
This is where l include some basic lines of code or queries or even some of the Dax expression used during my analysis.

### Queries and Answer 
Below are the SQL queries develop for this analysis 

1. which product category had the highest sales
,,,
   SQL
   SELECT product category,
   SUM(sale) As total_sales
   FROM order
   GROUP BY product_category 
   ORDER BY total_sales DESC
   LIMIT 1

2. What are the top3 and bottom3 regions in terms of sales

   
-- Top 3 regions
SELECT region, SUM(sales) AS total_sales
FROM orders
GROUP BY region
ORDER BY total_sales DESC
LIMIT 3;

-- Bottom 3 regions
SELECT region, SUM(sales) AS total_sales
FROM orders
GROUP BY region
ORDER BY total_sales ASC
LIMIT 3;

3. Total sales of appliances in Ontario

   SELECT SUM(sales) AS total_sales
FROM orders
WHERE product_category = 'Appliances' AND region = 'Ontario';

4. Increasing revenue from bottom10 customer
 To increase revenue feom the bottom10 customer KMS could consider 
. improving customer service and engagement 
. offering personalized discoun

6. Shipping method with highest cost

   SELECT shipping_method, SUM(shipping_cost) AS total_shipping_cost
FROM orders
GROUP BY shipping_method
ORDER BY total_shipping_cost DESC
LIMIT 1;




  
