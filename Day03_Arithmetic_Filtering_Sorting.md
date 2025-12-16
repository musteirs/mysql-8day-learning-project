# SQL Learning Journey – Day 3

## Focus of the Day

**Using Arithmetic Operators, Comparison Operators, Filtering, and Sorting Data**

Today’s work focuses on one of the most practical aspects of SQL: **asking precise questions from data**. This includes:

* Comparing values using conditions
* Performing calculations directly inside queries
* Filtering rows with `WHERE`
* Sorting results using `ORDER BY`

These skills are foundational for data analysis, reporting, and decision‑making.

---

## Exercise 1: Using Arithmetic and Comparison Operators

### Objective

Create a `products` table with a price column, retrieve products priced above 2000, and apply an 8% discount. The discounted price should be returned as `discount_price`.

### Why This Matters

In real business scenarios, prices are rarely static. Discounts, taxes, commissions, and markups are calculated dynamically. SQL allows you to perform these calculations **at query time**, without altering the original data.

This means:

* You preserve raw data integrity
* You generate flexible pricing insights
* You can simulate business rules instantly

---

### Sample Table Structure

```sql
CREATE TABLE Products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    price DECIMAL(10, 2)
);
```

---

### Query

```sql
SELECT
    product_name,
    price * 0.92 AS discount_price
FROM Products
WHERE price > 2000;
```

---

### Explanation

* `price > 2000` filters only premium products
* `price * 0.92` applies an 8% discount (100% − 8%)
* `AS discount_price` renames the calculated column for clarity

This approach keeps calculations transparent and readable.

---

## Exercise 2: Filtering and Sorting with WHERE and ORDER BY

### Objective

Create an `Employees` table and retrieve employees from the **Sales** department, sorted by their hire date.

### Why This Matters

Filtering and sorting are essential when working with large datasets. This type of query is commonly used for:

* HR analytics
* Team audits
* Performance and tenure analysis

Instead of scrolling through raw tables, SQL lets you extract exactly what you need, in the correct order.

---

### Sample Table Structure

```sql
CREATE TABLE Employees (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(100),
    department VARCHAR(50),
    hire_date DATE
);
```

---

### Query

```sql
SELECT
    employee_name,
    department,
    hire_date
FROM Employees
WHERE department = 'Sales'
ORDER BY hire_date;
```

---

### Explanation

* `WHERE department = 'Sales'` filters the dataset to a single department
* `ORDER BY hire_date` sorts employees from earliest to latest hire
* The result is a clean, logical list useful for analysis

---

## Key Takeaways from Day 3

* SQL can perform calculations without modifying stored data
* `WHERE` narrows down data to what truly matters
* `ORDER BY` improves readability and analysis flow
* Aliases (`AS`) make query output more meaningful

These concepts turn SQL from a storage language into an **analysis tool**.

---

## Challenges & Insights

### Challenges

* Remembering percentage calculations (e.g., 8% discount = `* 0.92`)
* Typos in column or table names can silently break queries
* Forgetting that `ORDER BY` defaults to ascending order

### Insights

* SQL thinks in sets, not rows — write queries with intention
* Clear naming (`discount_price`) improves understanding instantly
* Small queries reflect real‑world business logic

---

**End of Day 3**

This day builds the bridge between raw data and business insight — a critical milestone in learning SQL.
