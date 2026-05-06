# 🛒 Online Store Sales Analysis Dashboard


📌 Overview


This project presents an end-to-end Exploratory Data Analysis (EDA) and Power BI dashboard built on large-scale e-commerce data (13GB, 100M+ records).
The goal is to uncover business insights, customer behavior, and revenue drivers using real-world datasets.


## 📂 Datasets

eCommerce behavior data from multi category store - [![Dataset](https://img.shields.io/badge/Datasets-black)](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store?select=2019-Nov.csv)




🎯 Objectives
--

1. Analyze month-over-month revenue growth (Oct vs Nov)
2. Identify top-performing brands and categories
3. Understand customer spending behavior
4. Detect high-value customers and purchase patterns
5. Highlight data quality issues (Unknown categories/brands)
   
📊 Dashboard Features
-

🔝 KPIs
--
1. Total Revenue: 505M
2. Total Purchases: 1.65M
3. Total Customers: 697K
4. Growth Rate:  20%
5. Unknown Revenue Contribution:  10.45%
   
📈 Key Visuals

1. Revenue Trend Over Time
2. Revenue by Category
3. Revenue by Brand
4. Top Customers by Revenue
5. Top Customers by Purchase Frequency
6. Customer Segmentation (Low, Mid, High, Premium)
7. Revenue Contribution by Customer Segment
   
👥 Customer Segmentation
--
Customers are segmented based on total spending:

1. Low Value: < 100
2. Mid Value: 100 – 500
3. High Value: 500 – 1000
4. Premium: > 1000

This helps identify:

1. Core revenue drivers
2. High-value customer concentration
3. Spending distribution patterns
   
📌 Key Insights
-

1. Revenue increased by 20% from October to November
2. Apple dominates brand-level revenue contribution
3. Electronics is the top-performing category
4. Mid-value customers contribute the most revenue
5. A small group of customers drives high revenue (Pareto pattern)
6. Purchase frequency ≠ high spending (different customer behaviors)
7. 10% revenue comes from unknown categories/brands (data quality gap)
8. A mid-month spike suggests campaign or seasonal impact
   
⚙️ Technical Implementation
--
🔹 Tools Used
--
1. Power BI – Dashboard & Visualization
2. SQL Server / PostgreSQL – Data storage & querying
3. DAX – Calculations & KPIs
4. Power Query – Data cleaning & transformation
   
🔹 Data Processing
--
1. Handled large datasets (5GB–8GB files)
2. Filtered only purchase events for accurate analysis
3. Cleaned datetime fields (removed UTC issues)
4. Managed missing values using "Unknown" classification
5. Appended October & November datasets into a unified model
   
🔹 Key Measures (DAX)
--
1. Total Sales : 

       SUM(e_commerce_data[price])

3. Total Purchases :

       COUNTROWS(e_commerce_data)

3. Total Customers :

       DISTINCTCOUNT(e_commerce_data[user_id])

4. Growth % :

        VAR CurrentMonth = MONTH(MAX(e_commerce_data[event_time]))
        VAR CurrentRevenue =
    
       CALCULATE(
        [Total Sales],
        FILTER(
            ALL(e_commerce_data),
            MONTH(e_commerce_data[event_time]) = CurrentMonth
        )
       )

        VAR PreviousRevenue =
    
        CALCULATE(
            [Total Sales],
            FILTER(
                ALL(e_commerce_data),
                MONTH(e_commerce_data[event_time]) = CurrentMonth - 1
            )
        )


       RETURN
            DIVIDE(CurrentRevenue - PreviousRevenue, PreviousRevenue)

⚠️ Challenges Faced

1. Handling large datasets (100M+ rows)
2. Fixing datetime conversion issues
3. Managing Power BI performance limitations
4. Dealing with missing category/brand data
5. Building accurate growth calculations without a date table
   
🚀 Business Impact
--

This dashboard helps:

1. Identify revenue drivers
2. Understand customer value distribution
3. Improve marketing & targeting strategies
4. Highlight data quality improvements needed
5. Support data-driven decision making
   
📌 Conclusion
-

This project demonstrates the ability to:

1. Work with large-scale real-world data
2. Perform end-to-end data analysis
3. Build interactive dashboards
4. Extract actionable business insights
   
🔗 Future Improvements
-
1. Add date table for advanced time intelligence
2. Build cohort analysis (customer retention)
3. Implement predictive analytics (sales forecasting)
4. Enhance dashboard performance optimization
   
🙌 Author
-
Nikhil Sagar
Aspiring Data Analyst | Power BI | SQL | Excel

⭐ If You Found This Useful Consider starring ⭐ the repository to support the project.








