# home_sales_sparksql

In this project, I leverage PySpark to perform data analysis on home sales data. The project involves several key steps, including importing necessary PySpark SQL functions, reading data, creating temporary tables, performing data analysis, and optimizing query performance.

First, I import the necessary PySpark SQL functions to facilitate data manipulation and querying. Next, read the home_sales_revised.csv data file into a Spark DataFrame. Using this DataFrame, create a temporary table called sales, which allows us to run SQL queries directly on the DataFrame.

I address several questions using SparkSQL:

Average Price for Four-Bedroom Houses: Calculate the average price of four-bedroom houses sold for each year, rounding the results to two decimal places.

Average Price for Specific Home Criteria: Determine the average price of homes built each year that have three bedrooms and three bathrooms, again rounding the results to two decimal places.

Complex Home Criteria Analysis: Find the average price of homes built each year that meet the criteria of having three bedrooms, three bathrooms, two floors, and a size of at least 2,000 square feet, with results rounded to two decimal places.

Average Price by "View" Rating: Calculate the average price of homes per "view" rating, considering only those with an average home price of at least $350,000. Additionally, Determine the runtime for this query.

To optimize query performance, cache the home_sales temporary table. Verify if the table is cached, then rerun the query regarding average price by "view" rating, and compare its runtime to the uncached runtime.

Ppartition the formatted Parquet home sales data by the date_built field. This involves writing the data to Parquet format with partitioning. Create a temporary table for the Parquet data and rerun the average price by "view" rating query, comparing the runtime with the previous uncached runtime.

Finally, I uncache the home_sales temporary table and verify that it is uncached using PySpark. 
