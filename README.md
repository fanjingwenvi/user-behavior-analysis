# User Behavior Analysis

## Overview
This project builds an mordern end-to-end data pipeline to process 100M+ rows Taobao user interaction data. Data is ingested into an AWS S3 data lake, transformed with Spark and dbt, orchestrated via Airflow, loaded into AWS Redshift for scalable querying, and visualized through Tableau dashboards. It demonstrates how to design a scalable, cloud-based data platform using modern data engineering tools.

**Architecture Diagram** 
Mermaid 

## Business Background
Taobao is one of the biggest Chinese online shopping platform owned by Alibaba.
Business goals of the analysis:
Increase profit/sales.
Improve buyer and seller engagement.
KPIs include:
Conversion rate (view → favorite → cart → purchase).
Habit (daily and hourly active users)
Sengmentation(RFM model)
Preference(Top items and categories by engagement.)

## Dataset 
Source: Tianchi Taobao User Behavior Dataset
Size: 100,150,807 rows
Users: ~988k
Items: ~4.1M
Categories: ~9.4k
Features: user_id, item_id, category_id, behavior_type, timestamp

## Data Pipeline 

1. **Data Ingestion**  
   - Batch load from CSV → **AWS S3** (data lake).  
   - Optional: support for streaming in the future (Kafka/Kinesis).  

2. **Data Cleaning / ETL**  
   -  - **Spark** for large-scale batch ETL and **Airflow** for orchestration.
   - Handle nulls, duplicates, and anomalies.  
   - Schema validation.  
  
3. **Data Warehouse**  
   - **AWS Redshift** as the main warehouse.  
   - Partitioned/clustered tables for efficient querying.  
   - Optional: Redshift Spectrum for querying raw S3 data.  

4. **Analytic Engineering**  
   - **dbt** for SQL-based transformations.
   - Maintain modular, reusable transformation models. 

## Dashboard Visulization 

## Running the Project
Repo structure 
Environment consistency 
