# 🌦️ Weather ETL & ELT Data Pipeline

## 📌 Project Overview
This project demonstrates the design and implementation of **both ETL (Extract–Transform–Load) and ELT (Extract–Load–Transform) pipelines** for integrating and processing weather data from heterogeneous sources.

The pipeline combines **real-time weather data from an API** with **historical data from CSV files**, applies data validation and quality checks, and prepares analytics-ready datasets for business intelligence and analysis.

The project emphasizes **data quality, scalability, and modern data engineering practices**.

---

## 🎯 Objectives
- Build a complete **ETL pipeline** for structured data processing
- Implement an **ELT pipeline** for scalable and flexible transformations
- Integrate data from **API and file-based sources**
- Apply **data validation using Great Expectations**
- Compare ETL vs. ELT in terms of **speed, scalability, and efficiency**

---

## 📂 Data Sources
- **Visual Crossing Weather API**  
  - JSON-formatted real-time and historical weather data
- **CSV Files**  
  - Structured historical weather datasets

Both sources include timestamps and location metadata to support data lineage and integration.

---

## ⚙️ ETL Pipeline Architecture
**Extract → Transform → Load**

### 🔹 Extract
- API ingestion with retry logic and response caching
- CSV ingestion using Pandas with schema detection

### 🔹 Transform
- Column standardization and unit normalization
- Handling missing values and outliers
- Schema-aware merging of multi-source data
- Feature enrichment and metadata tagging

### 🔹 Load
- Cleaned data stored in **SQLite**
- Batch loading using Pandas and SQLAlchemy

---

## 🔄 ELT Pipeline Architecture
**Extract → Load → Transform**

### 🔹 Extract & Load
- Raw data loaded directly into **PostgreSQL staging tables**
- Separate staging tables for each data source

### 🔹 Validation
- Data quality checks using **Great Expectations**
- Schema validation and range checks (e.g., humidity 0–100)

### 🔹 Transform
- SQL-based transformations executed inside the data warehouse
- Data type enforcement, null handling, and standardization
- Creation of analysis-ready tables

---

## 📊 Data Validation & Quality
The project applies multi-layered data quality checks:
- Schema validation
- Statistical range checks

---

## 🛠️ Tools & Technologies
- **Python**
- **Pandas, NumPy**
- **SQLAlchemy**
- **Great Expectations**
- **SQLite**
- **PostgreSQL**
- **REST APIs**
- **SQL (in-database transformations)**

---

## 📈 Visualization
Processed datasets were visualized using **BI dashboards** to support analytics and decision-making.

---

## 🔍 ETL vs. ELT Comparison

| Aspect        | ETL                          | ELT                          |
|--------------|------------------------------|------------------------------|
| Processing   | Transform before load        | Transform after load         |
| Scalability  | Limited by processing layer  | Scales with data warehouse   |
| Flexibility  | Rigid schema                 | Schema-on-read               |
| Use Case     | Structured datasets          | Large & diverse datasets     |

---

## 🌍 Sustainability Impact
- **SDG 13 – Climate Action**: Supports accurate climate monitoring and weather analysis

---

## ✅ Key Skills Demonstrated
- ETL & ELT pipeline design
- API and CSV data integration
- Data validation and quality engineering
- SQL-based transformations
- Modern data engineering architecture

---
