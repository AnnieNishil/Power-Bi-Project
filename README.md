# Project Overview:

#### Title: Sales Performance Dashboard

#### Tools Used: Power BI, DAX, Power Query, Excel

#### Dataset: Superstore Sales Data 

#### Objective: To create an interactive dashboard to analyze sales performance across regions, categories, and time.


## Key Features & Visuals:


#### * Total Sales Overview

#### * A KPI card showing Total Sales for the selected period.

#### * Comparison: This year's sales vs. last year's sales (YoY Growth).

#### * Sales by Region

#### * A map or bar chart displaying total sales by region.

#### * Filterable with a slicer for Region.

#### * Sales by Category

#### * A pie chart or stacked bar chart showing sales distribution by product category.

#### *  Use slicers to filter by category and sub-category.

####  *Sales Trend Analysis

#### * A line chart showing monthly sales trends, with drill-down capability (Year > Quarter > Month).

#### * Top Products

#### * A table or bar chart showing the top 10 best-selling products based on total sales.

#### * Customer Segmentation

####  *A scatter plot that segments customers based on Total Sales and Number of Orders.

#### *  Filters to look at segments by Region and Category.



## Data Transformation & Cleaning:


#### Power Query:

#### Imported and cleaned data from an Excel file.

#### Removed unnecessary columns and handled missing data.

#### Created custom columns for Month, Year, and Sales Profit using Power Query Editor.

## DAX Calculations:


#### Total Sales:

Total Sales = SUM(Sales[SalesAmount])


#### YoY Growth:

YoY Growth = 
DIVIDE([Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])), 
CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])))

#### Sales by Region: 
Created dynamic measures using CALCULATE and FILTER functions to adjust based on slicers.



## Relationships:


#### Established relationships between Sales, Products, and Date tables.


## Power BI Visuals:


#### * KPI Cards for key metrics like Total Sales, Total Profit, and YoY Growth.

#### * Bar and Column Charts to display regional and product-based sales comparisons.

#### * Map Visual to represent sales geographically.

#### * Line Chart to show monthly sales performance.

#### * Slicers to filter by region, product, category, or time period.



## Challenges & Learnings:


#### Challenge: Handling missing or incomplete data in the source file.

#### Solution: Used Power Query to replace missing values with zero and removed irrelevant rows.

#### Challenge: Aggregating sales data across different time periods.

#### Solution: Created a custom Date Table and used DAX time intelligence functions like SAMEPERIODLASTYEAR().

#### Learning: Gained hands-on experience with DAX functions for time intelligence, calculated columns, and dynamic filtering.

## Final Outcome:

#### The Sales Performance Dashboard provides an intuitive view of total sales, regional performance, top products, and sales trends. It is an interactive dashboard where users can filter by region, category, and time period to get deeper insights.
