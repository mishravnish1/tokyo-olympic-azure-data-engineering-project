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






# 🏅 Tokyo Olympics Azure Data Engineering Project  

An **end-to-end Data Engineering pipeline** built on **Microsoft Azure** to analyze the Tokyo Olympics dataset.  
This project demonstrates how to build a modern data pipeline using cloud technologies with the **Medallion Architecture (Bronze → Silver → Gold)** approach.  

---

## 🚀 Architecture  

![Architecture](images/architecture.png)  
*(Add your architecture diagram in `images/architecture.png`)*  

**Workflow:**  
1. **Azure Data Factory (ADF):** Ingest raw CSV files into **Azure Data Lake Storage Gen2 (ADLS Gen2)**.  
2. **Azure Databricks (PySpark):** Transform raw data into curated form using Spark.  
3. **ADLS Gen2:** Store curated data (Silver/Gold layers).  
4. **Azure Synapse Analytics:** Query and analyze the curated data.  
5. **Power BI:** Build interactive dashboards for insights.  

---

## ⚙️ Tech Stack  

- **Cloud Platform:** Microsoft Azure  
- **Services Used:**  
  - Azure Data Factory  
  - Azure Data Lake Storage Gen2  
  - Azure Databricks (PySpark)  
  - Azure Synapse Analytics  
  - Power BI  

---

## 📊 Dataset  

The dataset used is from **Tokyo Olympics 2020**, containing multiple CSV files:  
- `Athletes.csv` → Athlete details  
- `Coaches.csv` → Coaches info  
- `EntriesGender.csv` → Gender participation  
- `Medals.csv` → Medal tally  
- `Teams.csv` → Team details  

*(Place datasets inside `data/` folder if available in repo)*  

---

## 🔄 Data Pipeline Workflow  

1. **Ingestion (Bronze Layer)**  
   - Data is ingested from CSV files into **Raw Zone** of ADLS using ADF.  

2. **Transformation (Silver Layer)**  
   - Using **Azure Databricks (PySpark)**:  
     - Clean null values  
     - Standardize column names  
     - Join multiple datasets  

3. **Aggregation (Gold Layer)**  
   - Store transformed, analytics-ready data into ADLS.  

4. **Analytics & Reporting**  
   - Query data using **Azure Synapse Analytics**.  
   - Create reports and dashboards in **Power BI**.  

---

## 📸 Project Screenshots  

👉 Add screenshots in an `images/` folder and link them here:  

- **Databricks Transformation Notebook:**  
  ![Databricks](images/databricks.png)  

- **Synapse Analytics Queries:**  
  ![Synapse](images/synapse.png)  

- **Power BI Dashboard (Medal Count, Top Nations, Gender Stats):**  
  ![Power BI](images/powerbi.png)  

---

## 🎯 Key Learnings  

- Building an end-to-end **ETL pipeline** on Azure  
- Applying the **Medallion Architecture** (Bronze/Silver/Gold)  
- Using **PySpark** for large-scale transformations  
- Querying curated data with **Azure Synapse**  
- Designing **Power BI dashboards** for insights  

---

## 🚀 How to Run  

1. Clone the repo  
   ```bash
   git clone https://github.com/mishravnish1/tokyo-olympic-azure-data-engineering-project.git
   cd tokyo-olympic-azure-data-engineering-project

