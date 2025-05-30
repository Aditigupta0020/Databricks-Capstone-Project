# Databricks-Capstone-Project
# 🚀 Databricks Capstone Project

This repository showcases a scalable Big Data pipeline built using **Apache Spark** on **Azure Databricks**, performing end-to-end **data ingestion**, **transformation**, and **analysis** on tweet data enriched with malicious actor insights.

---

## 📁 Project Overview

The project is divided into two key phases:

### 🔹 Part 1 – Data Ingestion
- Mounted and read nested **JSON** files from an **AWS S3** bucket using **Databricks File System (DBFS)**.
- Created structured **schemas** using `StructType` and `StructField` to define tweet data models.
- Processed and filtered null records, applied schema validation using custom testing functions (`dbtest`).
- Saved the cleaned and structured data as **Parquet files** for optimized querying and storage.

### 🔹 Part 2 – Transformation & Load
- Parsed tweeted URLs using a custom **UDF** (`getDomain`) that extracts domain names via regular expressions.
- Aggregated statistics to identify:
  - Most tweeted websites
  - Trending hashtags by day
- Merged new malicious user data (`badactors`) using **joins** and labeled suspicious activity with the `maliciousact` column.
- Repartitioned final datasets for scalable processing and loaded results into target tables.

---

## 🛠️ Technologies & Tools
- **Apache Spark** (PySpark)
- **Azure Databricks**
- **AWS S3** (as data source)
- **DBFS** (Databricks File System)
- **Spark SQL**
- **UDFs** (User Defined Functions)
- **JSON / Parquet** file formats
- **Schema Definition** using `StructType`, `StructField`
- **Regex** for domain parsing
- **Explode** function for nested arrays

---

## 📊 Features
- Schema-driven parsing of nested JSON data
- URL domain extraction with regular expressions
- Hashtag and URL trend analysis using aggregations
- Malicious user tagging through dataset merging
- End-to-end data validation using `dbtest` assertions
- Optimized file output with Parquet + partitioning

---




