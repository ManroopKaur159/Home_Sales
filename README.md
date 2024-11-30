Overview
This project analyzes home sales data using PySpark and answers specific queries about property prices 
based on various conditions like the number of bedrooms, bathrooms, floors, and square footage.

Dataset
The dataset used is home_sales_revised.csv, which is imported into a Spark DataFrame named home_sales_df. 
A temporary table, home_sales, is created from this DataFrame.

Analysis Steps
Read the CSV file home_sales_revised.csv into a Spark DataFrame named home_sales_df and created a temporary table home_sales.

PySpark SQL Queries: Calcualtion of the the following queries was performed-
1- Average Price for 4-Bedroom Homes by Year
2- Average Price for 3-Bedroom, 3-Bathroom Homes by Year Built
3- Average Price for Specific Homes with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet by year built.
4- Average Price of homes per "view" rating where the average home price is $350,000 or greater, and determined the query runtime.

Performance Optimization:
Caching: Cached the home_sales table and verified caching.
Partitioning: Partitioned the dataset by date_built and created a temporary table for the parquet-formatted data.

Query Runtime Comparison: Compared runtimes for the cached and uncached versions of the "view" rating query.
Uncaching: Uncached the home_sales table and verified its uncached status.

Variables Used
home_sales_df: Original DataFrame containing the home sales data.
home_sales: Temporary table created from home_sales_df.

SQL queries to calculate average prices were stored in variables such as:
average_4bedroom_price
avg_3bed3bath_price
avg_3_bed3bath_2floors_price
avg_price_by_view

