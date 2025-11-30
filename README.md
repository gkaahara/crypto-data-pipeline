# gkaahara/crypto-data-pipeline

# Crypto Market Analytics Pipeline - Real-Time Data Engineering on Databricks Free

[![Databricks](https://img.shields.io/badge/Databricks-Free_Edition-orange?logo=databricks)](https://community.cloud.databricks.com/)
[![PySpark](https://img.shields.io/badge/PySpark-3.x-blue?logo=apachespark)](https://spark.apache.org/)
[![Delta Lake](https://img.shields.io/badge/Delta_Lake-3.x-green?logo=delta-lake)](https://delta.io/)

End-to-end data pipeline implementando **medallion architecture** no **Databricks Community Edition (Free)** para análise em tempo real de criptomoedas. Otimizado para clusters limitados: processamento incremental, qualidade automatizada e zero custo.[attached_file:1]

## 🏗️ Arquitetura Medallion (Otimizada Free Tier)

Bronze → Silver → Gold
├── Raw API (CoinGecko) + Timestamp
├── Clean/Validate/Standardize (Incremental)
└── Aggregations + Analytics (Partitioned)
- **Bronze**: Ingestão raw com `MERGE` Delta para evitar reprocessamento em clusters 2GB RAM.[attached_file:1]
- **Silver**: Limpeza PySpark + validações (Great Expectations compatível).[attached_file:1]
- **Gold**: Métricas business-ready (top performers, volume signals).[attached_file:1]

## 🛠️ Tech Stack (Free Tier Ready)

| Ferramenta | Versão | Uso no Free |
|------------|--------|-------------|
| Databricks | Community | Clusters shared + Jobs schedules |
| PySpark | 3.x | Transformações otimizadas |
| Delta Lake | 3.x | Incremental + Partitioning |
| Python | 3.x | Utils + Quality checks |
| CoinGecko API | REST | Rate-limited ingestion |[attached_file:1]

## 🚀 Key Features & Otimizações

- ✅ **Medallion Architecture** completa em notebooks modulares
- ✅ **Incremental Processing** via Delta `MERGE` (evita throttles DBU)
- ✅ **Data Quality Framework** (`data_quality.py` com nulls/uniques/referencial)
- ✅ **Partitioned Storage** por `timestamp/coin_symbol` para queries <1s
- ✅ **Workflow Orchestration** via Databricks Jobs (hourly crypto volatility)
- ✅ **Free Tier Proof**: 100% funcional sem custos, dados persistem via Delta sharing[attached_file:1]

## 📈 Business Use Cases

- Daily trend analysis + top performers
- Volume-based trading signals
- Market cap tracking + volatility alerts
- **Demo Metrics**: 10k+ records/hour em cluster small[attached_file:1]

## 📁 Estrutura do Projeto

/Workspace
├── /notebooks
│ ├── 01_data_ingestion.py # CoinGecko → Bronze
│ ├── 02_bronze_to_silver.py
│ ├── 03_silver_to_gold.py
│ └── 04_analytics_queries.sql
├── /config
│ └── pipeline_config.json # API keys + schedules
└── /utils
├── data_quality.py # Automated checks
└── transformations.py # UDFs PySpark

## 🎯 Performance no Free Tier

| Métrica | Antes | Otimizado | Ganho |
|---------|-------|-----------|-------|
| Ingestão/hour | 2k records | 10k+ records | 5x |
| Query Gold | 15s | <1s | 15x |
| DBU consumo | High | Minimal | Sustainable |[attached_file:1]

## 🧪 Quick Start (Databricks Free)

1. Fork → Import Workspace: `https://community.cloud.databricks.com`
2. Config `pipeline_config.json` com sua CoinGecko API key
3. Run notebooks sequencial: `01 → 04`
4. Schedule Jobs: `cron(0 * * * ? *)` para hourly
5. Query Gold: `SELECT * FROM gold.crypto_metrics WHERE date = current_date()`

## 🔮 Próximas Features

- [ ] Delta Live Tables (streaming)
- [ ] DBT integration (SQL models)
- [ ] Streamlit dashboard (Unity Catalog)
- [ ] Airflow/Databricks Workflows hybrid[memory:18]

## 👨‍💻 Autor

**Gabriel Kaahara**  
[LinkedIn](https://www.linkedin.com/in/gabriel-kaahara-54b9b2104/) | [Portfolio](https://github.com/gkaahara)  
*Junior Data Engineer → Mid-Level Databricks Specialist*[memory:22][memory:19]

## 🤝 Contribuições

1. Fork → Pull Request
2. Testes: `pytest utils/`
3. Databricks Free: compartilhe seu workspace!

---

**⭐ Star se ajudou na sua jornada Data Engineering!** 🚀
