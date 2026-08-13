# databricks
Building a mordern data warehouse using databricks including ETL process modeling &amp; analytics

📊 Databricks Data Warehouse Project (Medallion Architecture)

🧾 Overview

This project implements a modern data warehouse on Databricks using the Medallion Architecture (Bronze, Silver, Gold layers). It processes raw retail data into clean, structured, and analytics-ready datasets for business intelligence and reporting.

🏗️ Architecture

![image alt](https://github.com/oladebo/databricks/blob/7735fa0bd6cfdb1a05c40429034a8b9d67429f19/Screen%20Shot%202026-04-02%20at%2019.40.02.png)









https://drive.google.com/file/d/1UI8U8iUvjVpod1Ivtbrgzt3TYlbgmobS/view?usp=drive_link

The project follows the Medallion Architecture:

🔹 Bronze Layer (Raw Data)
Ingests raw data from source systems (CSV!)
Stores data in its original format
Minimal transformation (schema enforcement, metadata addition)
Tables:

bronze_orders
bronze_customers

🔸 Silver Layer (Cleaned Data)
Performs data cleansing and transformation
Handles missing values, duplicates, and standardization
Applies business rules and joins datasets

Tables:

silver_orders
silver_customers

🟡 Gold Layer (Business Layer)
Aggregated and optimized for reporting
Designed using Star Schema
Supports dashboards and analytics

Tables:

fact_sales
dim_customers
dim_products

⚙️ Tech Stack
Databricks
Apache Spark (PySpark)
Delta Lake
DBFS (Databricks File System)
SQL Analytics / Databricks SQL
Power BI / Tableau (for reporting)



🚀 Data Pipeline Flow

1️⃣ Ingestion (Bronze)
Load raw files into Databricks
Store as Delta tables
Add ingestion timestamp


2️⃣ Transformation (Silver)
Clean data (null handling, formatting)
Deduplicate records
Join datasets

3️⃣ Modeling (Gold)
Create fact and dimension tables
Apply aggregations (sales, revenue)
Optimize for query performance


🧪 Transformations

Convert date formats
Standardize customer names
Handle missing values
Calculate total sales

🔄 Orchestration

Managed using Databricks Workflows
Scheduled jobs for:
Data ingestion
Data transformation
Data aggregation

📈 Use Cases

Sales performance analysis
Customer segmentation
Product performance tracking
Business reporting dashboards

🔐 Data Quality Checks

Null value validation
Duplicate removal
Schema enforcement
Data consistency checks

👨‍💻 By Oladebo A. Ayanniyi

