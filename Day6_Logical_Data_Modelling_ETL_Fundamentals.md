# SQL Learning Journey – Day 6

## Focus of the Day

**Logical Data Modeling and ETL Fundamentals**

Day 6 steps back from writing queries to understanding how data is **designed and moved**. This is where SQL meets system thinking: how tables relate and how data flows into a database.

---

## Exercise 1: Design a Basic Logical Data Model

### Objective

Outline the core tables for a simple e-commerce application, including:

* Customers
* Products
* Orders
* Order_Items

---

### Why This Matters

Before writing SQL queries, databases must be **well structured**. Logical data modeling helps:

* Reduce data duplication
* Maintain data integrity
* Make queries simpler and faster

A good model prevents problems before they happen.

---

### Logical Table Outline

```sql
Customers
- customer_id (PK)
- customer_name
- email
- phone_number

Products
- product_id (PK)
- product_name
- price

Orders
- order_id (PK)
- customer_id (FK)
- order_date

Order_Items
- order_item_id (PK)
- order_id (FK)
- product_id (FK)
- quantity
```

---

### Explanation

* Each table represents a single business entity
* Primary Keys (PK) uniquely identify records
* Foreign Keys (FK) create relationships between tables

This structure supports one-to-many relationships common in e-commerce systems.

---

## Exercise 2: Outline an ETL Process for Loading Customer Data

### Objective

Describe the steps required to **Extract, Transform, and Load (ETL)** customer data from a CSV file into a `Customers` table.

---

### Why This Matters

Most real-world data does not start inside databases. ETL ensures data is:

* Clean
* Consistent
* Ready for analysis

Understanding ETL is critical for analytics and data engineering roles.

---

### Sample ETL Steps

**Extract**

* Receive customer data as a CSV file
* Validate file structure and encoding

**Transform**

* Clean missing or invalid values
* Standardize column names and formats
* Remove duplicate records

**Load**

* Insert cleaned data into the `Customers` table
* Validate row counts and data accuracy

---

## Key Takeaways from Day 6

* Logical data models guide database structure
* Relationships are enforced using keys
* ETL pipelines ensure reliable data ingestion

---

## Challenges & Insights

### Challenges

* Deciding the correct table relationships
* Handling dirty or inconsistent source data

### Insights

* Good design simplifies everything downstream
* ETL is as important as querying

---

**End of Day 6**

Day 6 connects SQL skills to real system design and data workflows.
