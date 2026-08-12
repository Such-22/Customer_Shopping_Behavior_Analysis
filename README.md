# Customer Shopping Behavior Analysis
# Overview

This project analyzes customer shopping behavior to uncover patterns in spending, product preferences, discounts, and customer loyalty. It follows a complete data analytics workflow — from raw data to business-ready insights — using Python, SQL, Power BI, and Gamma for reporting.

The goal is to answer key business questions such as: Who are our highest-value customers? Which products and categories perform best? Does subscription status or discount usage influence spending? The final deliverables include a cleaned dataset, SQL analysis, an interactive Power BI dashboard, and a summary report/presentation.

# Dataset
- Source: Customer shopping behavior dataset (retail transactions)
- Size: ~3,900 records
- Key fields: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount, Location, Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Payment Method, Frequency of Purchases

# Tools & Technologies
- Python (Pandas) — data loading, cleaning, and exploratory data analysis (EDA)
- SQL (PostgreSQL / MySQL / SQL Server) — data querying and business analysis
- Power BI — interactive dashboard and data visualization
- SQLAlchemy — Python-to-database connection for loading cleaned data
Steps
# 1. Data Loading & EDA (Python)
- Loaded raw CSV data using Pandas
- Explored structure with .info(), .describe(), and .isnull().sum()
- Identified missing values and inconsistent column naming

# 2. Data Cleaning (Python)
- Filled missing review ratings using category-wise median
- Standardized column names (lowercase, underscores)
- Created derived features:
- age_group — binned into Young Adult, Adult, Middle-aged, Senior
- purchase_frequency_days — mapped purchase frequency labels (e.g., Weekly, Monthly) to numeric day values
- Removed redundant column (promo_code_used, which duplicated discount_applied)
- Exported the cleaned dataset and loaded it into a PostgreSQL database via SQLAlchemy

# 3. SQL Analysis
Wrote analytical queries to answer business questions, including:

- Revenue breakdown by gender and age group
- Customers who used discounts but still spent above average
- Top 5 highest-rated products
- Standard vs. Express shipping spend comparison
- Subscriber vs. non-subscriber spending behavior
- Products with the highest discount usage rate
- Customer segmentation (New, Returning, Loyal) based on purchase history
- Top 3 products per category using window functions (ROW_NUMBER())
- Relationship between repeat purchases and subscription status
- Revenue contribution by age group

# 4. Dashboard (Power BI)
Built an interactive Power BI dashboard to visualize:

- Revenue trends by category, gender, and age group
- Customer segmentation and subscription behavior
- Discount usage and its impact on spending
- Top-performing products and shipping preferences
- Slicers for dynamic filtering by category, location, and season

# 5. Reporting
- Summarized key findings in a written report
- Translating SQL and dashboard insights into a clear business narrative

# Dashboard
The Power BI dashboard provides an interactive view of customer behavior, including KPI cards, category performance, and customer segment breakdowns.

