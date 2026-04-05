
# 🏬 Customer Data Analysis Dashboard

## 🖼️ Dashboard Preview
![Dashboard](images/dashboard.png)


---


## 📌 Project Overview


This project analyzes customer purchasing behavior and revenue trends using an interactive Power BI dashboard.



It delivers actionable insights into:

Customer demographics

Product performance

Payment preferences

Sales distribution across locations



The goal is to transform raw transactional data into business-driven decisions.


---


## 🎯 Objectives


Identify key revenue-driving customer segments

Analyze product category performance

Understand payment behavior

Evaluate sales across shopping malls

Detect seasonal trends


---


## 🛠️ Tools Used


Power BI – Data visualization & dashboarding

SQL – Data analysis & transformation

Excel – Data cleaning & preparation


---


## 📊 Dashboard Features


Interactive filters (Age, Gender, Category, Location)

KPI cards for quick performance tracking

Clean, business-focused UI design

Drill-down capability for deeper insights


---


## 📊 Key Insights


Female customers contribute the highest share of revenue

Middle-aged customers are the most valuable segment

Clothing is the top-performing category

Cash is the most preferred payment method

Mall of Istanbul generates the highest revenue

Revenue shows clear seasonal fluctuations


---


## 📊 SQL Analysis


This section demonstrates how SQL was used to extract insights that power the dashboard and business decisions.

### 🔹 KPI Calculations


Objective: Evaluate overall business performance and efficiency per order.


```sql
SELECT
    SUM(quantity * price) AS total_revenue,
    SUM(quantity) AS total_quantity,
    COUNT(DISTINCT invoice_no) AS total_orders,
    SUM(quantity * price) / COUNT(DISTINCT invoice_no) AS avg_revenue_per_order
FROM cx_dataset;
```


💡 Business Insights:

Provides a high-level snapshot of business performance.

Average revenue per order highlights customer spending behavior.

A low average order value may indicate:

Need for bundling strategies
Opportunities for upselling / cross-selling

Helps evaluate sales efficiency per transaction


---


### 🟢 Revenue by Gender


Objective: Identify which customer segment contributes the most revenue.

```sql
SELECT
gender,
SUM(quantity * price) AS revenue
FROM cx_dataset
GROUP BY gender
ORDER BY revenue DESC;
```

💡 Business Insights:

Highlights top-performing customer segments.

Enables targeted marketing campaigns.

If one gender dominates:

Opportunity to rebalance strategy toward underperforming segment

Useful for personalized promotions and product positioning.


---


### 🟢 Revenue by Age Group


Objective: Understand purchasing power across different age segments.

```sql
SELECT
CASE
WHEN age BETWEEN 18 AND 25 THEN 'Young'
WHEN age BETWEEN 26 AND 39 THEN 'Adult'
WHEN age BETWEEN 40 AND 60 THEN 'Middle Aged'
ELSE 'Senior'
END AS age_group,
SUM(quantity * price) AS revenue
FROM cx_dataset
GROUP BY age_group
ORDER BY revenue DESC;
```


💡 Business Insights:

Identifies high-value age demographics.

Helps tailor:

Product offerings

Pricing strategies

Marketing channels

Example:

Younger customers → promotions & discounts

Older customers → premium or loyalty-focused strategies


---


### 🟢 Revenue by Product Category


Objective: Determine which product categories drive the most revenue.

```sql
SELECT
category,
SUM(quantity * price) AS revenue
FROM cx_dataset
GROUP BY category
ORDER BY revenue DESC;
```


💡 Business Insights:

Identifies top-performing products and underperformers.

Supports:

Inventory optimization

Product expansion decisions

High-performing categories → invest more (ads, stock, visibility)

Low-performing categories → reassess pricing or demand


---


### 🟢 Daily Revenue Trend


Objective: Analyze revenue patterns over time.

```sql
SELECT
DATE(STR_TO_DATE(invoice_date, '%d-%m-%Y')) AS sales_date,
SUM(quantity * price) AS daily_revenue
FROM cx_dataset
GROUP BY sales_date
ORDER BY sales_date;
```


💡 Business Insights:

Reveals sales trends and seasonality patterns.

Helps detect:

Peak sales days

Demand fluctuations

Enables:

Better forecasting

Improved staffing & inventory planning

Can uncover impact of campaigns or external events.


---



## 📂 Project Structure
```bash
customer-data-analysis-dashboard/
├── customer-dashboard.pbix
├── README.md
├── data/
├── images/
    └── dashboard.png
```

---

## 💡 Business Recommendations
- Focus on high-value customer segments to increase revenue  
- Optimize and expand top-performing product categories  
- Encourage adoption of digital payment methods  
- Improve performance in underperforming locations


---


## ▶️ How to Use
1. Download the `.pbix` file
2. Open it using Power BI Desktop
3. Interact with filters to explore insights


---
## 🧠 Skills Demonstrated
SQL (Aggregations, Grouping, Data Transformation)

Data Visualization (Power BI)

Business Analysis & Insight Generation

Dashboard Design & Storytelling


---

## 🚀 Final Note


This project demonstrates the ability to go beyond dashboards by combining technical SQL skills with business thinking, delivering insights that support data-driven decision-making.


---

## 👤 Author
Agberhiere Kesiena Perez 

Aspiring Data Analyst | Power BI | SQL  
