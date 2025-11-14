

# 📊 Sales Insights Project

### **SQL + Power BI | Data Analysis**

This project provides a simple but effective Sales Insights analysis using **SQL** for data exploration and **Power BI** for creating an interactive dashboard.
The goal is to understand sales trends, revenue patterns, and customer/product performance using a real-world–style dataset.

---

## 📁 **Project Files**

```
SQL PROJECT/
│
├── db_dump.sql            → SQL dump containing all tables
├── Power BI File.pbix     → Power BI dashboard
└── README.md              → Documentation
```

---

## 🧩 **Project Overview**

This project involves:

* Importing the provided **SQL database dump**
* Running SQL queries to understand the data
* Cleaning & converting sales values (USD → INR where required)
* Creating a Power BI dashboard to visualize:

  * Total revenue
  * Market-wise performance
  * Top customers
  * Product insights
  * Yearly & monthly trends

---

## 🛠️ **Technologies Used**

* **MySQL** (for querying the sales data)
* **Power BI Desktop** (for dashboard creation)
* **Data Modeling & DAX** (for calculated fields)

---

## 🗄️ **Database Description**

The SQL dump contains:

* **Customers** – customer information
* **Transactions** – sales orders, market code, amount, currency
* **Products** – product details
* **Date** – year, month, day fields

---

## 🔍 **Sample SQL Queries Used**

**1. Show all customers**

```sql
SELECT * FROM customers;
```

**2. Total revenue in INR**

```sql
SELECT 
    SUM(CASE 
            WHEN currency = 'USD' THEN sales_amount * 75
            ELSE sales_amount
        END) AS total_revenue_in_inr
FROM transactions;
```

**3. Sales in Chennai market**

```sql
SELECT * 
FROM transactions 
WHERE market_code = 'Mark001';
```

---

## 📈 **Power BI Dashboard**

The dashboard highlights:

* **Overall Revenue (INR normalized)**
* **Top 5 Customers**
* **Top Products**
* **Market Performance**
* **Monthly Trends**
* **Currency-adjusted Sales Amount**

You can open **Power BI File.pbix** to explore the visuals.

---

## ✔️ **Conclusion**

This project demonstrates how SQL and Power BI can be combined to convert raw sales data into actionable business insights.
It showcases essential skills for data analysis roles, including data cleaning, querying, currency normalization, visualization, and storytelling.

