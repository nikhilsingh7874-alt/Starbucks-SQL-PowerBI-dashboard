# ☕ Starbucks Sales & Customer Analytics Dashboard

![SQL](https://img.shields.io/badge/SQL-Database%20Design-blue?style=flat-square)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

> An end-to-end data analytics project simulating a Starbucks retail operation — from relational database design in SQL to an interactive Power BI dashboard uncovering sales trends, customer behavior, and product performance.

---

## 📸 Dashboard Preview

<!-- Add your dashboard screenshot below. Export it from Power BI Desktop (File > Export > Export to Image, or a simple screenshot) and save it as images/dashboard-preview.png in your repo. -->

![Dashboard Preview](https://github.com/nikhilsingh7874-alt/Starbucks-SQL-PowerBI-dashboard/blob/main/Screenshot%202026-09-03%20121156.png)

*Replace the image above with a screenshot of your Power BI dashboard for the full effect.*

---

## 📌 Project Overview

This project analyzes transactional retail data — customers, menu items, and sales — to answer key business questions:

- Which products drive the most revenue?
- How do sales vary by store, time, and payment mode?
- What does the customer base look like (age, gender, order type)?
- Who are the New vs. Regular customers, and how do they spend differently?

The workflow covers the full analytics pipeline: **database design → data modeling → SQL queries → Power BI visualization.**

---

## 🗂️ Dataset

The project uses three interconnected datasets:

| Dataset | Records | Description |
|---|---|---|
| `customers.csv` | 500+ | Customer ID, name, email, phone, age, gender |
| `items.csv` | 75+ | Menu item, category (beverage/food/bakery), calories, fat, carbs, fiber, protein |
| `sales.csv` | 10,000+ | Transaction ID, store ID, datetime, customer ID, item ID, quantity, price, total amount, payment mode, customer type |

**Key fields used for analysis:**
- `store_id` — multi-store performance comparison
- `payment_mode` — Cash, Card, UPI transaction trends
- `customer_type` — New vs. Regular segmentation
- `datetime` — time-of-day and daily sales trends
- `type` (items) — Beverage vs. Food vs. Bakery category performance

---

## 🏗️ Database Design

A normalized relational schema was built in SQL with proper primary and foreign key relationships:

```sql
customers (customer_id PK, customer_name, customer_email, customer_phone, customer_age, customer_gender)

items (id PK, item, calories, fat, carb, fiber, protein, type)

sales (transaction_id PK, store_id, datetime, customer_id FK, item_id FK,
       quantity, price, total_amount, payment_mode, customer_type)
```

- `sales.customer_id` → references `customers.customer_id`
- `sales.item_id` → references `items.id`

This structure enables clean joins across customer demographics, product details, and transaction history.

---

## 📊 Dashboard Features

Built in Power BI, the dashboard includes:

- 📈 **Sales Trends** — revenue over time, peak hours/days
- 🏪 **Store Performance** — comparison across store locations
- 🥤 **Top Products** — best-selling items by category
- 👥 **Customer Insights** — age, gender, and New vs. Regular breakdown
- 💳 **Payment Analysis** — Cash vs. Card vs. UPI usage trends
- 🍩 **Category Breakdown** — Beverage vs. Food vs. Bakery contribution to revenue

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **SQL** | Schema design, relationships, data insertion & querying |
| **Power BI** | Data modeling, DAX measures, interactive visualization |
| **CSV** | Raw source data for customers, items, and sales |

---

## 📁 Repository Structure

```
starbucks-sales-analytics/
├── data/
│   ├── customers.csv
│   ├── items.csv
│   └── sales.csv
├── sql/
│   └── SQL_Queries.txt
├── dashboard/
│   └── Starbuck_Dashboard.pbix
├── images/
│   └── dashboard-preview.png
└── README.md
```

---

## 🎯 Key Takeaways

This project strengthened practical skills in:
- Relational database design and normalization
- Writing and optimizing SQL queries
- Data modeling and DAX in Power BI
- Turning raw transactional data into actionable business insights

---

## 🚀 How to Use

1. Clone this repository
   ```bash
   git clone https://github.com/<your-username>/starbucks-sales-analytics.git
   ```
2. Open `dashboard/Starbuck_Dashboard.pbix` in **Power BI Desktop**
3. Explore the datasets in the `data/` folder
4. Review the schema and queries in `sql/SQL_Queries.txt`

---

## 📬 Contact

Feel free to connect or reach out if you have feedback or questions about this project!

- **LinkedIn:** [https://www.linkedin.com/in/nikhil-singh-48a676327/]
- **Email:** [nikhilsingh7874@gmail.com]

---

⭐ If you found this project useful or interesting, consider giving it a star!
