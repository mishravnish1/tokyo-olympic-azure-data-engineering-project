# 🏅 Tokyo Olympic Azure Data Engineering Project

## 📌 Project Overview
This project demonstrates an **end-to-end Azure Data Engineering pipeline** using the **Tokyo 2020 Olympics dataset**.  
It showcases how to **ingest, store, transform, analyze, and visualize** large datasets using Azure services.

The primary goal is to:
- Practice **modern data engineering concepts**
- Implement a **scalable medallion architecture** (Bronze → Silver → Gold layers)
- Use **Azure-native tools** for automation, processing, and analytics

---

## 📂 Dataset Information
The dataset contains information about:
- 🏃 Athletes
- 🏅 Medal standings
- 🧑‍🤝‍🧑 Teams
- 🏟️ Disciplines
- 🎯 Coaches
- 👩‍🔬 Entries by Gender

**Source:** [Tokyo Olympics Dataset - Kaggle](https://www.kaggle.com/datasets) *(or replace with your dataset source)*

---

## 🏗 Architecture

```plaintext
Data Source (CSV files)
        ↓
Azure Data Factory (ADF) - Ingestion
        ↓
Azure Data Lake Storage Gen2 (Bronze Layer - Raw Data)
        ↓
Azure Databricks (PySpark) - Data Cleaning & Transformation
        ↓
Azure Data Lake Storage Gen2 (Silver Layer - Clean Data)
        ↓
Azure Databricks / Synapse SQL - Business Aggregations
        ↓
Azure Data Lake Storage Gen2 (Gold Layer - Aggregated Data)
        ↓
Azure Synapse Analytics - Data Analysis
        ↓
Power BI - Visualization & Reporting
