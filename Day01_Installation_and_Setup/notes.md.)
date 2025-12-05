# Day 01 - Installation and Setup

## Introduction
Day 1 was dedicated to preparing the environment needed to work with MySQL. The goals were to:

- Install MySQL Community Server  
- Set up MySQL Workbench  
- Ensure server connectivity  
- Establish the initial schema  

This forms the foundation for all SQL practice in the following days.

---

## Downloading MySQL
MySQL Community Server was downloaded from the official site. The installer included:

- MySQL Server  
- MySQL Workbench  
- MySQL Shell  
- Configuration tools  

I chose the installer compatible with my operating system and used the default installation settings.

---

## Installing MySQL Server
Main steps completed during installation:

1. **Setup Type:** Selected Developer Default to include all necessary tools.  
2. **Account Configuration:**  
   - Created a root password  
   - Left authentication method as “Use Strong Password Encryption”  
3. **Windows Service Setup:**  
   - Installed MySQL as a Windows service  
   - Enabled automatic startup  
4. **Configuration:** Applied all settings successfully  

After installation, the MySQL server started automatically.

---

## Installing and Configuring MySQL Workbench
I opened MySQL Workbench and created a new connection:

- **Connection Name:** Local MySQL Server  
- **Hostname:** localhost  
- **Port:** 3306  
- **Username:** root  
- **Password:** saved securely  

Workbench successfully tested the connection to the MySQL server.

---

## Verifying the Server Connection
To ensure the server was working:

- Connected to MySQL through Workbench  
- Confirmed the SQL editor loaded without errors  
- Executed a test query:

```sql
SELECT VERSION();

Creating My First Schema
Method 1 - Using Workbench GUI

1. Click Create a new schema

2. Enter schema name: testdb

3. Apply changes

4. Verify the schema appears in the list of databases

Method 2 - Using SQL
  CREATE SCHEMA test2db;

Both methods successfully created working databases.

First SQL Executions

To verify the schema:

  SHOW DATABASES;
  USE testdb;

Creating a Sample Table
  CREATE TABLE sampletable (
      id INT,
      name VARCHAR(50)
  );

Dropping the Sample Table
  DROP TABLE sampletable;

Basic SQL Practice
Created a students table and performed sample insertions and queries:

  CREATE TABLE students (
      studentid INT PRIMARY KEY,
      firstname VARCHAR(30),
      lastname VARCHAR(30)
  );
  
  INSERT INTO students (studentid, firstname, lastname)
  VALUES 
  (1, 'Adnan', 'Musa'),
  (2, 'Mustapha', 'Musa'),
  (3, 'Mustapha', 'Adnan');
  
  SELECT * FROM students;
  SHOW TABLES;
  DROP TABLE students;

Summary

By the end of Day 1, I had:

Installed a working MySQL Community Server

Set up MySQL Workbench

Verified server connectivity

Created testdb and test2db schemas

Executed basic SQL commands

Practiced creating, inserting, querying, and deleting tables

This setup provides a solid environment to continue learning SQL.
