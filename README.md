## Sales Analytics Capstone Project

Prepared by: Bindu Madhuri Chalasani
Tools Used: Power BI, Snowflake, SQL, Excel
Project Type: Power BI Capstone Project (Dual Interactive Dashboards)
Dataset: Global Sales Data (2003–2005, 326 Orders, 121 Customers)

📌 **Project Overview**

This capstone project delivers two interactive Power BI dashboards to analyze global sales data (2003–2005).
The dataset was sourced from a Snowflake data warehouse, transformed with SQL queries, and visualized in Power BI.

**The dashboards provide:**

Sales Summary Dashboard – Executive-level KPIs and regional trends.

Sales Insight & Performance Dashboard – In-depth analysis of customer behavior, product performance, order statuses, and customer distribution.

Together, they enable strategic decision-making with dynamic filters and interactive visuals.

🎯 **Objectives**

Provide a Sales Summary Dashboard for high-level KPIs and trends.

Deliver a Sales Insight & Performance Dashboard for detailed insights.

Enable interactive exploration using slicers (year, region, product line, order status, category).

Demonstrate end-to-end BI skills: data extraction → transformation → modeling → visualization.

📂 **Dataset Description**

Source: Snowflake Data Warehouse

Records: 326 orders, 121 customers

Period: 2003–2005

Key Attributes: Order ID, Customer Name, Product Line, Order Status, Sales Amount, Profit, Year, Country, Customer Count

Challenges: Inconsistent formats, missing 2003 sales data, aggregation across multiple dimensions

⚙️ **Technical Approach**
1. Data Extraction & Transformation

SQL queries in Snowflake for cleaning & aggregation

Computed sales, profit, profit ratios, and counts

Standardized formats and handled missing values

**Sample SQL Query:**

SELECT
    YEAR(order_date) AS order_year,
    product_line,
    country,
    COUNT(DISTINCT customer_id) AS customer_count,
    SUM(sales_amount) AS total_sales,
    SUM(profit) AS total_profit
FROM sales_data
GROUP BY YEAR(order_date), product_line, country;

2. **Data Modeling**

Star Schema in Power BI

**DAX Measures:**

Total Sales → SUM(sales_data[total_sales])

Profit Ratio → DIVIDE(SUM(sales_data[total_profit]), SUM(sales_data[total_sales]), 0)

Customer Count → DISTINCTCOUNT(sales_data[customer_id])

3. **Dashboard Design**

Visuals: Pie charts, bar charts, treemaps, tables

Filters: Year, Region, Product Line, Order Status, Category

Styling: Consistent color theme & professional layout

4. **Delivery**

Dashboards exported as PBIX files

Documentation & user guide included

📊 **Dashboard Details**
1. **Sales Summary Dashboard**

KPIs: Total Sales ($62.3M), Total Profit ($1.5M), Profit Ratio (2.4%)

**Visuals:**

Sales by product category (Technology 37.7%)

Regional profit ratios (Canada, Central Africa leading)

Salesperson performance table

**Insights:**

Technology is top revenue driver

Central Asia shows negative margins

Peak sales in 2014, decline in 2015

2. Sales Insight & Performance Dashboard

KPIs: 326 Orders, 121 Customers

**Visuals:**

Orders by year (2004 → 45%)

Orders by status (Shipped → 93%)

Orders by product line (Classic Cars → 170)

Top 10 customers (Euro+ Shopping Channel → $720K)

Customer distribution by country (Germany → 13, France → 12)

**Insights:**

Classic Cars dominate order volume

High order fulfillment (93%) → efficiency

Sales decline from 2004 → 2005

💡 **Business Impact**

Strategic: Identify top-performing markets & products

Trend Monitoring: Spot declining sales & negative margins

Efficiency: Validate fulfillment success rate

Customer Focus: Recognize top customers for retention

🚀 **Outcomes & Skills Demonstrated**

End-to-End BI Pipeline: ETL → Modeling → Visualization

SQL, DAX, Power BI interactivity

Data storytelling & actionable insights

Strategic & operational alignment


🔮 **Future Enhancements**

Add missing 2003 data for trend completeness

Include profit metrics in Insight Dashboard

Integrate real-time data streams

Optimize for mobile viewing

📌 **Conclusion**

This project demonstrates technical expertise (SQL, Snowflake, Power BI, DAX) and business acumen through actionable dashboards that support data-driven decisions.
