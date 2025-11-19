# Azure-Based Demand Forecasting & Capacity Optimization System

This project demonstrates an end-to-end modern data engineering pipeline using **Azure Data Factory**, **Azure Databricks**, **Snowflake**, **Google BigQuery**, **Azure Data Lake Storage**, and **Power BI**.  
The goal is to integrate logistics and operations datasets, build a lakehouse architecture (Bronze–Silver–Gold), and apply machine learning for demand forecasting and capacity planning.

---

## 🚀 Architecture Overview

**Data Sources**
- Logistics dataset → **Snowflake**
- Operations dataset → **Google BigQuery (GCP)**

**ETL Pipeline (Azure Data Factory)**
- Ingest Snowflake data → ADLS Raw Zone  
- Ingest BigQuery data → ADLS Raw Zone  
- Trigger notebooks for:
  - **Bronze Layer** (raw → structured)
  - **Silver Layer** (cleaning, transformations)
  - **Gold Layer + ML** (feature engineering, Random Forest model)

**Lakehouse (Databricks)**
- Bronze: ingestion & parquet storage  
- Silver: cleaning, renaming, type casting  
- Gold: model training + predictions  

**Analytics (Power BI)**
- Connected to ADLS Gold tables  
- Built interactive dashboards:  
  - Delivery performance  
  - Supplier cost analysis  
  - Demand forecasting  
  - Warehouse utilization  

---


