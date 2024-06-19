# Athletic Sales Analysis

This project involves analyzing sales data to gain insights into the sales of athletic wear over two years. The analysis includes determining top-selling cities, retailers, and specific sales periods for women's athletic footwear.

> Table of Contents
Background
Files
Instructions
Steps
Combine and Clean the Data
Determine which Region Sold the Most Products
Determine which Region had the Most Sales
Determine which Retailer had the Most Sales
Determine which Retailer Sold the Most Women's Athletic Footwear
Determine the Day with the Most Women's Athletic Footwear Sales
Determine the Week with the Most Women's Athletic Footwear Sales
Dependencies
Usage

#### Background
This analysis identifies which U.S. cities sold the most athletic wear over two years, determines the retailers with the greatest total sales, and finds the top days and weeks for women's athletic footwear sales.

### Files
`athletic_sales_2020.csv`

`athletic_sales_2021.csv`

### Instructions
Follow the instructions to clone the repository, import data, clean and analyze the data, and push the changes to GitHub or GitLab.

### Steps
1. Combine and Clean the Data
2. Import the CSV files and read them into DataFrames.
3. Combine the DataFrames using an inner join and reset the index.
4. Check for null values and correct data types.
5. Convert the invoice_date column to a datetime data type.
6. Determine which Region Sold the Most Products
7. Use groupby or pivot_table to create a multi-index DataFrame with region, state, and city.
8. Aggregate the data and rename the column to reflect the aggregation.
9. Sort the results to show the top five regions, states, and cities with the greatest number of products sold.
10. Determine which Region had the Most Sales
11. Use groupby or pivot_table to create a multi-index DataFrame with region, state, and city.
12. Aggregate the data and rename the column to reflect the aggregation.
13. Sort the results to show the top five regions, states, and cities with the greatest total sales.
14. Determine which Retailer had the Most Sales
15. Use groupby or pivot_table to create a multi-index DataFrame with retailer, region, state, and city.
14. Aggregate the data and rename the column to reflect the aggregation.
16. Sort the results to show the top five retailers with the greatest total sales.
17. Determine which Retailer Sold the Most Women's Athletic Footwear
16. Filter the DataFrame to include only women's athletic footwear sales.
17. Use groupby or pivot_table to create a multi-index DataFrame with retailer, region, state, and city.
18. Aggregate the data and rename the column to reflect the aggregation.
19. Sort the results to show the top five retailers with the most women's athletic footwear sales.
20. Determine the Day with the Most Women's Athletic Footwear Sales
31. Create a pivot table with invoice_date as the index and total_sales as the values.
32. Rename the aggregated column to reflect the aggregation.
33. Resample the data into daily bins and calculate the total sales for each day.
34. Sort the results to show the top 10 days with the most sales.
35. Determine the Week with the Most Women's Athletic Footwear Sales
36. Resample the pivot table into weekly bins and calculate the total sales for each week.
37. Sort the results to show the top 10 weeks with the most sales.

### Dependencies
pandas
"Install the required dependencies using:"

``pip install pandas``

# Clone the repository:

``git clone https://github.com/rmsreis/athletic_sales_analysis.git``

Navigate to the project directory:

``cd athletic_sales_analysis``

Run the provided Python script to perform the analysis:

``python``

```
import pandas as pd

# Load your DataFrame here
combined_sales_df = pd.read_csv('athletic_sales_2020.csv')
combined_sales_df = pd.concat([combined_sales_df, pd.read_csv('athletic_sales_2021.csv')]).reset_index(drop=True)

# Convert 'invoice_date' to datetime
combined_sales_df['invoice_date'] = pd.to_datetime(combined_sales_df['invoice_date'])

# Analysis steps here...

```