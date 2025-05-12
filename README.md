# Pizza Sales Dashboard

### Dashboard Link : 

## Problem Statement

The pizza business operates in a dynamic and customer-driven market, yet lacks clear visibility into its sales performance across products, time periods, and categories. Without an integrated system to track and analyze key performance indicators—such as total revenue, average order value, best-selling products, and sales trends by day or month—management cannot make data-informed decisions to optimize operations and marketing efforts. This dashboard aims to solve that problem by providing a comprehensive view of pizza sales data, enabling stakeholders to monitor performance, identify high- and low-performing items, and uncover actionable insights to drive business growth.

### Steps followed 

- Step 1: Load Dataset
The pizza_sales.csv file was loaded into SSMS Desktop and Power BI. This dataset includes key fields such as order ID, date, pizza name, category, quantity, price, and total amount.

- Step 2: Power Query Data Profiling
In Power Query Editor, under the View tab, the following options were enabled:

Column Distribution

Column Quality

Column Profile

These tools helped analyze data quality and detect anomalies or inconsistencies in the dataset.

- Step 3: Entire Dataset Profiling
The column profiling mode was changed to “Based on entire dataset” instead of the default 1000 rows to ensure complete and accurate insights during data preparation.

- Step 4: Null/Empty Values Check
Data quality review showed no major issues. Null values were found in a few records of the Total Price column, likely due to missing quantities or unit prices, and were excluded from calculations as they represented less than 1% of the dataset.

- Step 5: Theme Selection
A built-in theme was selected under the View > Themes section to improve the report's visual appeal and consistency.

- Step 6: Visual Filters (Slicers)
Slicers were added for easy filtering across the following dimensions:

- Pizza Category

- Order Date

- Pizza Name

These slicers allow users to dynamically explore sales by different product types and time periods.

- Step 7: KPI Cards
KPI cards were added to display core performance metrics:

Total Revenue

Total Quantity Sold

Average Order Value

Total Orders

DAX measures were created to calculate each of these KPIs.

- Step 8: Sales by Pizza Type
A bar chart was used to show total revenue by pizza name, helping identify the top-selling and lowest-performing pizzas.

- Step 9: Category-Wise Performance
A pie chart was used to represent the percentage share of revenue by pizza category (Classic, Supreme, Veggie).

- Step 10: Time-Based Trends
A line chart was created to show monthly sales trends, revealing seasonality and peak sales periods. A date hierarchy (Year > Month) was used for granularity.

- Step 11: Size Preference
A stacked column chart was added to visualize revenue by pizza size (S, M, L, XL, XXL), highlighting customer preferences across different size offerings.

- Step 12: Calculated Columns
A new column was created to group orders by time of day using the Order Time field:

DAX
Copy
Edit
Time Slot = 
SWITCH(TRUE(),
    HOUR(pizza_sales[Order Time]) < 11, "Morning",
    HOUR(pizza_sales[Order Time]) < 16, "Afternoon",
    HOUR(pizza_sales[Order Time]) < 21, "Evening",
    "Late Night")
- Step 13: Additional Measures
Several DAX measures were added for more detailed insights:

Average Pizza Price

Average Pizzas per Order

Total Revenue by Category

Revenue Growth Rate (Month-over-Month)
- 
- Step 14: Branding
Two text boxes were added to the report:

Brand Name (e.g., Bella Pizza Co.)

Company Tagline (e.g., "Slice of Happiness")

Company logo was added using the Insert > Image option, and a colored rectangle was used for header styling.

- Step 15: Report Publication
The completed dashboard was published to Power BI Service, allowing real-time sharing and access for business stakeholders.

📈 Insights from Pizza Sales Dashboard
Total Orders: [e.g., 5000+ orders processed]

Top 3 Selling Pizzas: [e.g., Pepperoni, BBQ Chicken, Margherita]

Best Performing Category: [e.g., Supreme Pizzas accounted for 45% of total revenue]

Peak Order Time: [e.g., Evenings between 6-9 PM]

Most Preferred Size: [e.g., Large (L) pizza size]

Average Order Value: [e.g., $23.45]

Seasonal Trend: [e.g., Sales peaked in December and July]

# Snap Of Dashboard

![Snap](https://github.com/user-attachments/assets/6f396b3e-07c2-49a9-b806-a1942832a467)
