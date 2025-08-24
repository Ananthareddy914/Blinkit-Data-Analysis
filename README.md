 Blinkit Data Analytics — Step by Step Process

This project analyzes Blinkit sales data using Excel → EDA → Power BI.
The aim was to clean, explore, and visualize the data to understand sales trends, customer behavior, and city/category performance.

Tools Used

Excel → Initial data checks, cleaning, handling missing values.

EDA (Exploratory Data Analysis) → Finding trends, patterns, and outliers.

Power BI → Data modeling, DAX measures, and dashboard building.

 Step by Step Process
 Data Understanding & Cleaning (Excel)

Imported datasets into Excel (Orders, Order_Items, Customers, Products, Cities).

Checked row counts and column names.

Found issues like:

Numbers stored as text → converted to numbers.

Mixed date formats → standardized to YYYY-MM-DD.

Extra spaces in city/product names → cleaned using TRIM.

Removed duplicates and filled/handled null values.

Mistake I made: At first, I ignored data types, so totals didn’t add up correctly in Power BI.
Fix: Went back and corrected the data formats in Excel.

Exploratory Data Analysis (EDA)

Looked at data trends manually in Excel (filters, pivot tables, charts).

Identified key patterns:

Which cities/categories contribute the most sales.

Peak order times (morning, afternoon, evening).

Average Order Value (AOV).

Repeat vs new customers (if signup dates available).

Mistake I made: I jumped into Power BI without proper EDA → dashboards looked confusing.
Fix: Did a round of pivot tables/charts in Excel first to get clarity.

 Data Modeling in Power BI

Imported cleaned data into Power BI.

Created a star schema:

FactOrders (transactions with order_id, product_id, qty, unit_price, status, date)

DimDate, DimCustomer, DimProduct, DimCity

Defined proper one-to-many relationships (Dim → Fact).

Mistake I made: Initially built fact at “order level” and also tried to bring product details — got wrong totals.
Fix: Rebuilt fact at line-item level (order + product) so totals stayed consistent.

 Dashboard Building

Executive Dashboard

KPIs: Revenue, Orders, AOV, Customers, Growth %

Revenue trend over time

Top cities and categories

Orders by hour

Deep Dive Dashboard

City × Category matrix

Product ranking table with conditional formatting

Drillthrough to city-level view

Mistake I made: Put too many visuals on one page → messy.
Fix: Split into two clear pages (Overview + Deep Dive).

 Key Insights

Evening hours (6–10 PM) are peak for orders.

Top 3–5 cities contribute most revenue.

Essentials/FMCG categories drive repeat orders.

AOV varies by city → opportunities for bundling and cross-sell.

Month-start & weekends show higher orders.
