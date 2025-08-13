# YouTube Data Analysis – End-to-End AWS Data Engineering Project

## 📌 Overview
This project implements a **complete data engineering pipeline** to analyze **YouTube trending video data** and help a hypothetical client optimize **ad campaign strategies**.  
The pipeline handles **data ingestion, transformation, storage, and visualization** using **AWS cloud services**.

---

## 🎯 Project Goals
- **Data Ingestion**: Ingest data from multiple sources (JSON & CSV from Kaggle dataset).
- **ETL Pipeline**: Transform raw data into a clean, analytics-ready format.
- **Data Lake**: Store raw, cleansed, and analytical datasets in **AWS S3**.
- **Data Visualization**: Build an interactive dashboard to derive actionable insights.

---

## 🛠 Technologies & Tools
- **AWS S3** – Data lake for raw, cleansed, and analytics data
- **AWS Glue** – ETL jobs & schema cataloging
- **AWS Lambda** – Transform nested JSON into flat Apache Parquet
- **Amazon Athena** – Query S3 data with SQL
- **Amazon QuickSight** – Dashboard creation & data visualization
- **Apache Parquet** – Efficient columnar storage
- **PySpark** – Data processing & transformation
- **AWS CLI** – Data upload & management

---

## 📂 Project Pipeline
### **1. Data Ingestion & Setup**
- Download YouTube trending videos dataset from **Kaggle**.
- Upload raw **JSON & CSV** files to **AWS S3** using AWS CLI.
- Use **AWS Glue Crawler** to automatically detect schema.
- Transform JSON to **Parquet** using **AWS Lambda**.

### **2. Data Processing & Cleaning**
- Catalog CSV schema using AWS Glue.
- Resolve **schema mismatches** between JSON and CSV (e.g., `category_id` type).
- Create Glue ETL jobs to convert CSV to Parquet, partitioned by region.
- Handle encoding issues and filter for CA, GB, and US data.

### **3. Final Preparation & Visualization**
- Join JSON & CSV cleansed datasets using Glue Studio.
- Store the **final analytics dataset** in a dedicated S3 bucket.
- Query data with Athena and connect to QuickSight.
- Build dashboards showing **views, likes, and regional performance**.

---

## 📊 Dashboard Insights
The QuickSight dashboard includes:
- **Top viewed videos** by region
- **Likes-to-views ratio** for engagement analysis
- **Category-wise performance**
- **Regional trend analysis**

---

## 🚀 How to Run This Project
1. **Set up AWS Account** and configure IAM user with required permissions.
2. Install and configure **AWS CLI**.
3. Create **S3 Buckets** for raw, cleansed, and analytics data.
4. Download Kaggle dataset and upload to the raw S3 bucket.
5. Run **Glue Crawlers** and **Lambda functions** for transformation.
6. Create **ETL Jobs** in AWS Glue to process and join datasets.
7. Use **Amazon Athena** for querying.
8. Connect Athena to **Amazon QuickSight** and create visualizations.

---

## 📁 Dataset
- **Source**: [Kaggle - YouTube Trending Video Dataset](https://www.kaggle.com/datasets/datasnaek/youtube-new)
- **Format**: JSON & CSV
- **Size**: ~200 MB

---

## 📷 Project Architecture
