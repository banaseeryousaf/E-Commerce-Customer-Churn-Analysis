# E-Commerce-Customer-Churn-Analysis
PROJECT OVERVIEW
 
This project analyzes customer churn patterns in the e‑commerce domain using SQL. The goal is to uncover drivers of customer attrition (such as tenure, complaints, payment modes, and order behavior) and provide actionable insights for reten

TOOLS USED
- MySQL (for data cleaning, transformation, and analysis)
- SQL Workbench (query execution )


DATASET

Source : https://drive.google.com/uc?export=download&id=1iKKCze_Fpk2n_g3BIZBiSjcDFdFcEn3D

Key Columns: CustomerID, Tenure, PreferredPaymentMode, PreferredOrderCat, CityTier, WarehouseToHome, HoursSpentOnApp, OrderCount, CouponUsed, SatisfactionScore, CashbackAmount, Churn, Complain
  
 STEPS FOLLOWED
 
 Data Cleaning

- Imputed missing values (mean for numeric columns, mode for categorical).
- Removed outliers in WarehouseToHome (>100 km).
- Standardized categorical values (e.g., “COD” → “Cash on Delivery”).
  
 Data Transformation
 
- Renamed inconsistent columns (PreferedOrderCat → PreferredOrderCat).
- Created derived fields:
- ComplaintReceived (Yes/No)
- ChurnStatus (Active/Churned)
- Dropped redundant columns (Churn, Complain).
  
 Data Exploration & Analysis
 
- Count of churned vs active customers.
- Average tenure & cashback of churned customers.
- Churn breakdown by complaints, city tier, and preferred order category.
- Preferred payment mode among active customers.
- Segmentation by marital status, warehouse distance, and satisfaction score.
- Top 3 order categories by average cashback.
- Categorization of customers by warehouse distance (Very Close, Close, Moderate, Far).

 Relational Table Design
 
- Created customer_returns table to track refund behavior.
- Joined with customer data to analyze churned customers with complaints and returns.

 KEY INSIGHTS
  
- Customers with complaints showed a significantly higher churn rate.
- City Tier‑1 had the highest churn in Laptop & Accessory category.
- Credit Card was the most preferred payment mode among active customers.
- Single customers preferring mobile phones showed higher order amount hikes.
- Top cashback categories: Electronics, Fashion, and Groceries.
- Warehouse distance strongly correlated with churn — farther customers churned more.

 FILES INCLUDED
  
- E-Commerce Customer churn db.sql – Table creation and sample data insertion. 
- ecomm.sql – Cleaned and transformed dataset.
- README.md – Project description.


