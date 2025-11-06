# Crypto Market Analytics Pipeline - Real-Time Data Engineering

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)]()
[![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apache-spark&logoColor=white)]()
[![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=flat)]()

## 📊 Project Overview
End-to-end data pipeline built on Databricks implementing medallion architecture 
for real-time cryptocurrency market analytics.

## 🏗️ Architecture
- **Bronze Layer**: Raw API data ingestion with timestamping
- **Silver Layer**: Data cleaning, validation, and standardization
- **Gold Layer**: Business-ready aggregations and analytics

## 🛠️ Tech Stack
- Databricks Free Edition
- PySpark
- Delta Lake
- Python 3.x
- REST APIs (CoinGecko)

## 🚀 Key Features
✅ Medallion architecture implementation
✅ Data quality framework with automated checks
✅ Incremental processing with Delta Lake
✅ Workflow orchestration
✅ Partitioned storage for optimization
✅ Real-time market analytics

## 📈 Business Use Cases
- Daily market trend analysis
- Top performers identification
- Volume-based trading signals
- Market cap tracking


## 📚 Project Structure
/Workspace
├── /notebooks
│   ├── 01_data_ingestion
│   ├── 02_bronze_to_silver
│   ├── 03_silver_to_gold
│   └── 04_analytics_queries
├── /config
│   └── pipeline_config.json
└── /utils
    ├── data_quality.py
    └── transformations.py


## 🎯 Results & Insights
[Screenshots and findings...]

## 👨‍💻 Author
Gabriel Kaahara
https://www.linkedin.com/in/gabriel-kaahara-54b9b2104/
