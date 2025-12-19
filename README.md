# KafkaLake Forecast — Dockerized Data Engineering & ML Pipeline

KafkaLake Forecast is a **production-style data engineering project** that demonstrates how to build a **real-time streaming pipeline with Kafka**, process data using **Spark Structured Streaming**, store it in a **Delta Lakehouse**, orchestrate workflows with **Airflow**, validate data quality with **Great Expectations**, and train a **machine learning model for demand forecasting**.

This project is built **step by step**, following real-world data engineering best practices.

---

## 🎯 Project Goal
Predict product demand (J+1) using real-time and historical sales data in order to:
- improve stock planning
- reduce shortages
- support business decisions

---

## 🧱 Tech Stack
- **Kafka** – real-time streaming ingestion
- **Spark Structured Streaming (PySpark)** – data processing
- **Delta Lake** – Lakehouse architecture (Bronze / Silver / Gold)
- **MinIO (S3)** – object storage
- **Airflow** – pipeline orchestration
- **Great Expectations** – data quality validation
- **XGBoost / LightGBM** – machine learning forecasting
- **FastAPI** – model serving
- **Docker & Docker Compose** – full environment setup

---

## 🏗️ High-Level Architecture
1. Sales events are produced to **Kafka**
2. Spark Streaming consumes Kafka data → **Bronze Delta tables**
3. Airflow runs daily jobs:
   - Bronze → Silver (cleaning & validation)
   - Silver → Gold (feature engineering)
   - Train & evaluate ML model
   - Promote best model to production
4. FastAPI serves predictions through an API

---

## 🗂️ Lakehouse Layers
- **Bronze**: raw Kafka events
- **Silver**: cleaned and validated data
- **Gold**: aggregated features for ML

---

## ⛓️ Airflow DAG (Daily)
- `bronze_to_silver`
- `validate_data_quality`
- `build_gold_features`
- `train_ml_model`
- `evaluate_model`
- `promote_model`
- `api_smoke_test`

---

## 🚧 Project Status
This project is under active development:

- [x] Repository initialization
- [ ] Dockerized base stack (Kafka, Spark, MinIO, Airflow)
- [ ] Kafka producer
- [ ] Spark streaming ingestion
- [ ] Data quality checks
- [ ] ML training & evaluation
- [ ] API serving

---

## 👤 Author
**Saad Bouali**  
Master Big Data & Cloud Computing  
📍 Casablanca, Morocco  
🔗 LinkedIn: https://linkedin.com/in/saad-bouali  
📧 Email: saadbouali2020@gmail.com
