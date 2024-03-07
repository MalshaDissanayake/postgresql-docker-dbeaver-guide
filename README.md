 # PostgreSQL Docker Container Setup Guide

This repository serves as a comprehensive guide for setting up a Docker container with PostgreSQL and connecting to it using DBeaver. Whether you're a beginner or looking to refresh your knowledge, this guide will walk you through the process step by step.

## Table of Contents
1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Setup Instructions](#setup-instructions)
    - [Step 1: Setting Up Docker Container with PostgreSQL](#step-1-setting-up-docker-container-with-postgresql)
    - [Step 2: Connect to PostgreSQL Instance Using DBeaver](#step-2-connect-to-postgresql-instance-using-dbeaver)
    - [Step 3: Creating a Table in PostgreSQL](#step-3-creating-a-table-in-postgresql)
    - [Step 4: Inserting Data into the Table](#step-4-inserting-data-into-the-table)
    - [Step 5:Running a Query to get a preview of table](#step-5-running-a-query-to-get-a-preview-of-table)
    - [Step 6: Running a Query](#step-6-running-a-query)
4. [Conclusion](#conclusion)

## Introduction
This guide aims to simplify the process of setting up a PostgreSQL environment using Docker and connecting to it using DBeaver. It covers everything from installation to performing basic database operations.

## Prerequisites
Before you begin, ensure you have the following:
- Docker installed on your system.
- If not, you can download it from [Download_Docker](https://docs.docker.com/manuals/)
- Access to the internet to download Docker images and DBeaver tool

## Setup Instructions
Follow the steps below to set up your PostgreSQL environment and connect to it using DBeaver.

### Step 1: Setting Up Docker Container with PostgreSQL
1. Pull the PostgreSQL Docker image.
   Open your terminal (or command prompt) and execute the following command to pull the official PostgreSQL Docker image:
   ```
   docker pull postgres
   ```
3. Create a Docker container with PostgreSQL.
   ```
   docker run --name my_postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
   ```
 
Replace "mysecretpassword" with your desired password.

### Step 2: Connect to PostgreSQL Instance Using DBeaver
1. Download and install DBeaver.
    Link:[Download_DBeaver](https://dbeaver.io/download/)
2. Configure a new database connection to PostgreSQL.<br>
   Open DBeaver and click on "Database" in the top menu.<br>
   Choose "New Database Connection."<br>
   Select "PostgreSQL" as the database type.<br>
   Set the connection details:<br>

    Host: localhost<br>
    Port: 5432<br>
    Database: postgres<br>
    Username: postgres<br>
    Password: (the password you set in the Docker command)<br>
    Click "Test Connection" to ensure it's successful, then click "Finish" to save the connection.

### Step 3: Creating a Table in PostgreSQL
1. Use DBeaver to create a new table named `userlogs`.<br>
```
CREATE TABLE userlogs (
    user_id VARCHAR(255),
    exam_id VARCHAR(255),
    page_id VARCHAR(255),
    q_id VARCHAR(255),
    a_id VARCHAR(255),
    is_correct BOOLEAN,
    ets TIMESTAMP
);
```


### Step 4: Inserting Data into the Table
1. Manually insert data into the `userlogs` table.<br>
```
INSERT INTO userlogs (user_id, exam_id, page_id, q_id, a_id, is_correct, ets)
VALUES
    ('user1', 'exam1', 'page1', 'q1', 'a1', true, NOW()),
    -- Repeat similar lines for the remaining rows
    ('user20', 'exam20', 'page20', 'q20', 'a20', false, NOW());
```

### Step 5: Running a Query to get a preview of table
Write and execute the below query to check the table that you created.
```
SELECT * FROM userlogs;
```


### Step 6: Running a Query
1. Write and execute a query to retrieve data from the `userlogs` table.
   ```
   SELECT is_correct , 
	count(user_id) as numberOfUsers
   FROM userlogs
   Group BY is_correct
   ```
## Conclusion
Congratulations! You have successfully set up a Docker container with PostgreSQL, created a table, inserted data, and connected to PostgreSQL using DBeaver. You are now ready to explore more advanced database operations.

Feel free to contribute to this repository by providing feedback or suggesting improvements.
