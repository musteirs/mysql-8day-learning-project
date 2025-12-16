# SQL Learning Journey – Day 7

## Focus of the Day

**Logical Schema Design and Data Import**

Day 7 brings everything together by translating a logical idea into a structured schema and loading real data into the database. This is where planning meets execution.

---

## Exercise 1: Create a Logical Schema for the Project

### Objective

Outline tables and relationships for a small system such as an **Inventory** or **CRM** application.

---

### Why This Matters

A logical schema defines how data is organized and connected. It ensures:

* Consistent data storage
* Clear relationships between entities
* Scalability as the system grows

This step prevents structural issues before data is inserted.

---

### Sample Logical Schema (Inventory System)

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
- stock_quantity

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

* Each table represents a distinct entity
* Primary keys uniquely identify records
* Foreign keys establish relationships between tables

This schema supports reporting, inventory tracking, and customer analysis.

---

## Exercise 2: Import Data from CSV

### Objective

Load customer data from a CSV file into the `Customers` table.

---

### Why This Matters

Most databases are populated from external files. Knowing how to import CSV data allows SQL users to:

* Move data from spreadsheets into databases
* Prepare data for querying and analysis
* Support ETL and migration workflows

---

### Sample CSV Format

```csv
customer_id,customer_name,email,phone_number
1,John Doe,john@example.com,08012345678
2,Jane Smith,jane@example.com,08087654321
```

---

### Load Data Query (MySQL)

```sql
LOAD DATA INFILE 'path_to_csv.csv'
INTO TABLE Customers
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

---

### Explanation

* `LOAD DATA INFILE` imports data efficiently
* Field and line terminators define CSV structure
* `IGNORE 1 ROWS` skips the header row

This method is faster than manual inserts for large datasets.

---

## Key Takeaways from Day 7

* Logical schemas guide data organization
* CSV imports connect external data to databases
* Proper structure simplifies analysis

---

## Challenges & Insights

### Challenges

* File path permissions when loading CSV files
* Matching CSV columns to table structure

### Insights

* Good schema design saves time later
* Data loading is a core database skill

---

**End of Day 7**

Day 7 completes the transition from planning to working with real data.
