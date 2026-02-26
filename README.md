# 📊 Online Book Store Sales & Customer Analysis (SQL Project)

## 📌 Project Overview

This project focuses on analyzing sales data from an online bookstore using SQL.  
The objective is to extract meaningful business insights related to revenue performance, customer behavior, product trends, and inventory management.

The analysis was performed using relational database concepts such as JOINs, aggregations, subqueries, GROUP BY, HAVING, and window functions.

---

## 🎯 Business Problem

The online bookstore wanted to:

- Understand overall sales performance
- Identify top-selling books and genres
- Detect high-value and repeat customers
- Track monthly revenue trends
- Monitor stock levels and prevent stockouts

Raw transactional data was stored in relational tables, and SQL was used to transform this data into actionable business insights.

---

## 🗂️ Database Structure

The database consists of three tables:

### 1️⃣ Books Table
-  Book_ID SERIAL PRIMARY KEY,
-    Title VARCHAR(100),
-   Author VARCHAR(100),
-    Genre VARCHAR(50),
-    Published_Year INT,
-    Price NUMERIC(10, 2),
-    Stock INT
  

### 2️⃣ Customers Table
- Customer_ID SERIAL PRIMARY KEY,
-  Name VARCHAR(100),
-  Email VARCHAR(100),
-  Phone VARCHAR(15),
-  City VARCHAR(50),
-  Country VARCHAR(150)

### 3️⃣ Orders Table
- Order_ID SERIAL PRIMARY KEY,
-  Customer_ID INT REFERENCES Customers(Customer_ID),
-  Book_ID INT REFERENCES Books(Book_ID),
-  Order_Date DATE,
-  Quantity INT,
- Total_Amount NUMERIC(10, 2)

Relationships:
- Customers → Orders (One-to-Many)
- Books → Orders (One-to-Many)

---

## 🛠️ Tools & Technologies Used

- SQL (PostgreSQL)
- Relational Database Concepts
- GitHub for version control and documentation

---

## 📊 Key Analysis Performed

1) Retrieve all books in the "Fiction" genre
2) Find books published after the year 1950
3) List all customers from the Canada
4) Show orders placed in November 2023
5) Retrieve the total stock of books available
6) Find the details of the most expensive book
7) Show all customers who ordered more than 1 quantity of a book
8) Retrieve all orders where the total amount exceeds $20
9) List all genres available in the Books table
10) Find the book with the lowest stock
11) Calculate the total revenue generated from all orders

Advance Queries
1) Retrieve the total number of books sold for each genre
2) Find the average price of books in the "Fantasy" genre
3) List customers who have placed at least 2 orders
4) Find the most frequently ordered book
5) Show the top 3 most expensive books of 'Fantasy' Genre
6) Retrieve the total quantity of books sold by each author
7) List the cities where customers who spent over $30 are located
8) Find the customer who spent the most on orders
9) Calculate the stock remaining after fulfilling all orders

## 🧠 SQL Concepts Demonstrated

- SELECT, WHERE
- GROUP BY & HAVING
- ORDER BY
- INNER JOIN & LEFT JOIN
- Aggregate Functions (SUM, COUNT, AVG)
- Subqueries
- Window Functions (RANK)
- Date Functions
- Foreign Key Relationships

---

## 📈 Key Business Insights

- Identified top customers contributing a significant percentage of total revenue.
- Determined the highest-performing book genre.
- Analyzed monthly sales trends to identify peak revenue months.
- Detected low-stock and out-of-stock books to prevent lost sales.
- Found repeat customers to support customer retention strategies.

---

## 💡 Business Recommendations

- Increase inventory for high-demand books.
- Introduce loyalty programs for repeat customers.
- Run promotional campaigns during low-revenue months.
- Provide discounts on slow-moving inventory.
- Focus marketing efforts on top-performing genres.

---

## 📁 Project Structure

```
online-bookstore-sql-analysis/
│
├── schema.sql              # Database structure
├── data.sql                # Sample dataset
├── analysis_queries.sql    # All SQL analysis queries
├── insights.md             # Business insights & findings
└── README.md               # Project documentation
```

---

## 🚀 How to Run This Project

1. Create a new database.
2. Run `schema.sql` to create tables.
3. Run `data.sql` to insert sample data.
4. Execute queries from `analysis_queries.sql` to perform analysis.

---

## 🎤 project Explanation (Short Summary)

In this project, I analyzed online bookstore data using SQL to evaluate revenue performance, customer behavior, and product trends.  
I applied joins, aggregations, subqueries, and window functions to generate business insights and provide data-driven recommendations.

---

## 📌 Future Improvements

- Add Power BI dashboard for visualization
- Perform customer segmentation analysis
- Add advanced KPI metrics
- Optimize queries using indexing

---

## 👨‍💻 Author

Mritunjay Kumar  
Aspiring Data Analyst | SQL | Data Analytics  

---

