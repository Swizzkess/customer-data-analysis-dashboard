
# 🏬 Customer Data Analysis Dashboard

## 🖼️ Dashboard Preview
![Dashboard](images/dashboard.png)

---

📌 Project Overview


This project analyzes customer purchasing behavior and revenue trends using an interactive Power BI dashboard.



It delivers actionable insights into:

Customer demographics

Product performance

Payment preferences

Sales distribution across locations



The goal is to transform raw transactional data into business-driven decisions.

🎯 Objectives
Identify key revenue-driving customer segments

Analyze product category performance

Understand payment behavior

Evaluate sales across shopping malls

Detect seasonal trends

🛠️ Tools Used
Power BI – Data visualization & dashboarding

SQL – Data analysis & transformation

Excel – Data cleaning & preparation

📊 Dashboard Features
Interactive filters (Age, Gender, Category, Location)

KPI cards for quick performance tracking

Clean, business-focused UI design

Drill-down capability for deeper insights

📊 Key Insights
Female customers contribute the highest share of revenue

Middle-aged customers are the most valuable segment

Clothing is the top-performing category

Cash is the most preferred payment method

Mall of Istanbul generates the highest revenue

Revenue shows clear seasonal fluctuations

📊 SQL Analysis


This section demonstrates how SQL was used to extract insights that power the dashboard and business decisions.

### 🔹 KPI Calculations
```sql
SELECT
    SUM(quantity * price) AS total_revenue,
    SUM(quantity) AS total_quantity,
    COUNT(DISTINCT invoice_no) AS total_orders,
    SUM(quantity * price) / COUNT(DISTINCT invoice_no) AS avg_revenue_per_order
FROM cx_dataset;
```
---

## 📊 Key Insights
- Female customers contribute the majority of total revenue  
- Middle-aged customers generate the highest revenue  
- Clothing is the top-performing category  
- Cash is the most preferred payment method  
- Mall of Istanbul leads in total revenue  
- Revenue shows seasonal fluctuations  

---

## 🚀 Features
- Interactive filters (Age, Gender, Category, Location)  
- KPI cards for quick insights  
- Clean and business-focused dashboard design  

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


## ▶️ How to Use
1. Download the `.pbix` file
2. Open it using Power BI Desktop
3. Interact with filters to explore insights

---


## 💡 Business Recommendations
- Focus on high-value customer segments to increase revenue  
- Optimize and expand top-performing product categories  
- Encourage adoption of digital payment methods  
- Improve performance in underperforming locations  

---

## 👤 Author
Agberhiere Kesiena Perez 

Aspiring Data Analyst | Power BI | SQL  
