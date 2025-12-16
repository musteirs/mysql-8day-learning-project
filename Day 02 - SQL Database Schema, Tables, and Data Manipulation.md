# Day 02 - SQL Exercises: Database Schema, Tables, and Data Manipulation

## Exercise 1: Database Schema and Table Creation
**Objective:** Design and create a schema with tables using appropriate data types.

**Instructions & Solutions:**

1. **Create a database in MySQL Workbench**
2. Use the new database
3. Create students, courses, and enrolments tables
4. Review tables
  ## Exercise 2: Modify Table and Insert Data
**Instructions & Solutions:**
1. **Add email column to the students table:**
2. **Insert data into students, courses, and enrolments tables**
```sql
CREATE DATABASE school_db;
USE school_db;
CREATE SCHEMA school2_db;
USE school2_db;

CREATE TABLE students (
    student_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    birth_date DATE
);

CREATE TABLE courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100),
    credits INT
);

CREATE TABLE enrolments (
    enrolment_id INT PRIMARY KEY,
    student_id INT,
    course_id INT,
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);
SHOW TABLES;

ALTER TABLE students
ADD COLUMN email VARCHAR(50);

INSERT INTO students (student_id, first_name, last_name, birth_date, email)
VALUES (1, 'Adnan', 'Musa','1999-10-10', 'adnan@gmail.com');

INSERT INTO courses (course_id, course_name, credits)
VALUES 
    (101, 'Mathematics', 3),
    (102, 'History', 2);

INSERT INTO enrolments (enrolment_id, student_id, course_id)
VALUES (1, 1, 101);
