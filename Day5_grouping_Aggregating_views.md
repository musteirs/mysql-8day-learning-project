# SQL Learning Journey – Day 5

## Focus of the Day

**Grouping Data, Aggregation, and Views**

Day 5 moves into summarizing data and saving reusable queries. These skills are critical when working with reports, dashboards, and recurring business questions.

---

## Exercise 1: Group Data and Filter with HAVING

### Objective

Use a `Sales` table to calculate total sales per salesperson and display only those whose total sales exceed **$1000**.

---

### Why This Matters

Raw transaction data is rarely useful on its own. Businesses care about **summaries**—total sales, averages, and performance per person or region.

`GROUP BY` allows SQL to aggregate data, while `HAVING` filters results **after aggregation**, something `WHERE` cannot do.

---

### Sample Table Structure

```sql
CREATE TABLE Sales (
    sale_id INT PRIMARY KEY,
    salesperson_id INT,
    amount DECIMAL(10,2)
);
```

---

### Query

```sql
SELECT
    salesperson_id,
    SUM(amount) AS total_sales
FROM Sales
GROUP BY salesperson_id
HAVING total_sales > 1000;
```

---

### Explanation

* `SUM(amount)` calculates total sales per salesperson
* `GROUP BY salesperson_id` defines how the data is aggregated
* `HAVING total_sales > 1000` filters aggregated results

This query highlights **top-performing salespeople**, a common business requirement.

---

## Exercise 2: Creating a View

### Objective

Create a view that shows only employees in the **Engineering** department.

---

### Why This Matters

Views act like saved queries. They:

* Simplify complex SQL
* Improve consistency across reports
* Enhance security by exposing only necessary data

Views are widely used in analytics and production systems.

---

### Sample Table Structure

```sql
CREATE TABLE Employees (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(100),
    department VARCHAR(50)
);
```

---

### Create View Query

```sql
CREATE VIEW Engineering_Employees AS
SELECT
    employee_name,
    department
FROM Employees
WHERE department = 'Engineering';
```

---

### Explanation

* The view stores a reusable query
* Filters employees to only Engineering department
* Can be queried like a regular table

Example:

```sql
SELECT * FROM Engineering_Employees;
```

---

## Key Takeaways from Day 5

* `GROUP BY` summarizes data
* `HAVING` filters aggregated results
* Views improve reuse, clarity, and maintainability

---

## Challenges & Insights

### Challenges

* Confusing `WHERE` and `HAVING`
* Forgetting that views do not store data, only queries

### Insights

* Aggregation turns data into insight
* Views help standardize analysis across teams

---

**End of Day 5**

Day 5 introduces summary analysis and reusable logic — core skills for analytics and reporting.
