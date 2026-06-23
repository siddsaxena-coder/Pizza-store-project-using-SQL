# 🍕 Pizza Sales Analysis using SQL

A data analysis project that explores pizza sales data using SQL to uncover business insights such as revenue trends, best-selling pizzas, order distribution, and category performance.

## 📌 Project Overview

This project demonstrates how SQL can be used to analyze transactional sales data and answer real-world business questions. The analysis covers basic, intermediate, and advanced SQL concepts including:

- Joins
- Aggregate Functions
- GROUP BY
- Subqueries
- Window Functions
- Ranking Functions

---

## 📂 Dataset Structure

The project uses four tables:

### Orders
Contains order information.
- order_id
- order_date
- order_time

### Order_Details
Contains ordered items.
- order_details_id
- order_id
- pizza_id
- quantity

### Pizzas
Contains pizza size and price information.
- pizza_id
- pizza_type_id
- size
- price

### Pizza_Types
Contains pizza category and names.
- pizza_type_id
- name
- category

---

## 🛠 SQL Concepts Used

- SELECT Statements
- Aggregate Functions (COUNT, SUM, AVG)
- INNER JOIN / LEFT JOIN
- GROUP BY
- ORDER BY
- Subqueries
- Window Functions
- RANK()
- OVER()
- Date and Time Functions

---

## 📊 Business Questions Solved

### Basic Analysis

✔ Retrieve the total number of orders placed.

✔ Calculate the total revenue generated.

✔ Identify the highest-priced pizza.

✔ Find the most common pizza size ordered.

✔ List the top 5 most ordered pizza types.

---

### Intermediate Analysis

✔ Find total quantity sold for each pizza category.

✔ Analyze order distribution by hour.

✔ Determine category-wise distribution of pizzas.

✔ Calculate average pizzas ordered per day.

✔ Find top 3 pizza types based on revenue.

---

### Advanced Analysis

✔ Calculate percentage contribution of each category to total revenue.

✔ Analyze cumulative revenue over time.

✔ Find top 3 pizzas by revenue within each category using window functions.

---

## 📈 Key Insights

- Identified peak order hours to understand customer demand.
- Discovered the highest revenue-generating pizzas.
- Analyzed category-wise sales performance.
- Used cumulative revenue analysis to study business growth over time.
- Applied ranking functions to identify top-performing pizzas within each category.

---

## 🧑‍💻 Technologies Used

- SQL
- MySQL
- Window Functions
- Aggregate Functions

---

## 📁 Project Files

```
📦 Pizza-Sales-Analysis
│
├── Questions.txt          # Business questions
├── answers.txt            # SQL solutions
├── Dashboard.twb          # Tableau dashboard
├── Presentation.pdf       # Project presentation
├── Presentation.pptx      # Project slides
└── README.md
```

---

## 🚀 Sample Query

```sql
SELECT
    T.name,
    SUM(D.quantity * P.price) AS Revenue
FROM order_details D
LEFT JOIN pizzas P
    ON D.pizza_id = P.pizza_id
LEFT JOIN pizza_types T
    ON P.pizza_type_id = T.pizza_type_id
GROUP BY T.name
ORDER BY Revenue DESC
LIMIT 3;
```

---

## 📊 Dashboard

The Tableau dashboard provides interactive visualizations for:

- Revenue Analysis
- Peak Order Hours
- Category Performance
- Top Selling Pizzas
- Sales Trends

---

## 🎯 Project Objective

To demonstrate practical SQL skills by solving business problems and extracting meaningful insights from sales data.

---

## ⭐ Skills Demonstrated

- Data Analysis
- SQL Query Writing
- Data Aggregation
- Window Functions
- Business Intelligence
- Analytical Thinking
- Problem Solving

---

### If you found this project useful, don't forget to ⭐ star the repository!
