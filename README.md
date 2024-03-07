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
    - [Step 5: Running a Query](#step-5-running-a-query)
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
   `print(docker pull postgres)'
3. Create a Docker container with PostgreSQL.

### Step 2: Connect to PostgreSQL Instance Using DBeaver
1. Download and install DBeaver.
2. Configure a new database connection to PostgreSQL.

### Step 3: Creating a Table in PostgreSQL
1. Use DBeaver to create a new table named `userlogs`.

### Step 4: Inserting Data into the Table
1. Manually insert data into the `userlogs` table.

### Step 5: Running a Query
1. Write and execute a query to retrieve data from the `userlogs` table.

## Conclusion
Congratulations! You have successfully set up a Docker container with PostgreSQL, created a table, inserted data, and connected to PostgreSQL using DBeaver. You are now ready to explore more advanced database operations.

Feel free to contribute to this repository by providing feedback or suggesting improvements.
