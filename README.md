# 🚀 Real-Time Social Media Sentiment Analysis Pipeline

A cloud-based **Real-Time Data Engineering Pipeline** built using **Azure Event Hub, Azure Databricks, Delta Lake, Apache Airflow, dbt, Power BI, and Microsoft Azure** to ingest, process, transform, and analyze social media data using the **Medallion Architecture (Bronze, Silver, Gold)**.

---

# 📖 Project Overview

This project demonstrates an end-to-end real-time data engineering solution that ingests social media events, processes streaming data using Azure Databricks Structured Streaming, stores data in Delta Lake, orchestrates workflows with Apache Airflow, and visualizes business insights using Power BI.

The pipeline transforms raw streaming data into analytics-ready datasets by implementing the **Bronze, Silver, and Gold** architecture.

---

# 🎯 Business Objective

Organizations require real-time analytics from social media platforms to understand:

- Customer Sentiment
- Trending Topics
- User Engagement Patterns
- Influencer Activity
- Business Impact of Social Media Discussions

This project provides an automated analytics platform that converts raw social media streams into actionable business insights.

---

# 🏗️ Solution Architecture

```
Producer Scripts
        │
        ▼
Azure Event Hub
        │
        ▼
Azure Databricks Structured Streaming
        │
        ▼
Bronze Layer (Raw Data)
        │
        ▼
Silver Layer (Cleaned & Validated Data)
        │
        ▼
Gold Layer (Business Aggregates)
        │
        ▼
Power BI Dashboard
```

> **Note:** Replace the above diagram with your architecture image if available.

---

# ⚙️ Technology Stack

| Category | Technology |
|-----------|------------|
| Programming | Python |
| Streaming | Azure Event Hub |
| Processing | Apache Spark / PySpark |
| Data Platform | Azure Databricks |
| Storage | Delta Lake |
| Data Modeling | dbt |
| Workflow Orchestration | Apache Airflow |
| Testing | Pytest |
| Visualization | Power BI |
| Cloud Platform | Microsoft Azure |
| Version Control | Git & GitHub |

---

# 📂 Dataset Components

The pipeline processes the following datasets:

| Dataset | Description |
|----------|-------------|
| Tweets | Social media posts |
| Sentiment | Sentiment scores and classifications |
| Trends | Trending hashtags and topics |
| User Metadata | User profile information |
| Valid Tweets | Validated tweet records |

---

# 🥉 Bronze Layer

## Purpose

Store raw streaming data exactly as received from Azure Event Hub.

### Activities

- Read streaming data from Azure Event Hub
- Store raw JSON records
- Add ingestion timestamp
- Maintain source metadata
- Preserve original schema

### Output Tables

- bronze_tweets
- bronze_sentiment
- bronze_trends
- bronze_user_metadata
- bronze_valid_tweets

---

# 🥈 Silver Layer

## Purpose

Clean, standardize, and validate streaming data.

### Activities

- Remove duplicate records
- Handle missing values
- Perform schema validation
- Convert data types
- Apply business validation rules
- Perform data quality checks

### Output Tables

- silver_tweets
- silver_sentiment
- silver_trends
- silver_user_metadata
- silver_valid_tweets

---

# 🥇 Gold Layer

## Purpose

Generate business-ready analytical datasets.

### Activities

- Build Star Schema
- Create Dimension Tables
- Create Fact Tables
- Aggregate business metrics
- Generate KPIs

### Dimension Tables

- dim_user
- dim_date
- dim_topic
- dim_sentiment

### Fact Table

- fact_socialmedia

### Aggregated Tables

- gold_sentiment_summary
- gold_trending_topics
- gold_user_engagement
- gold_geographic_analysis

---

# 🔄 Data Pipeline Workflow

### Step 1 – Producer Scripts

Generate real-time social media events.

**Producer Files**

- tweets-hub.py
- sentiment-hub.py
- trends-hub.py
- user-metadata-hub.py
- valid-tweets-hub.py

### Step 2

Publish streaming events to Azure Event Hub.

### Step 3

Azure Databricks Structured Streaming continuously reads data from Event Hub.

### Step 4

Bronze pipelines store raw data into Delta Lake tables.

### Step 5

Silver pipelines clean, validate, and standardize data.

### Step 6

Gold pipelines create business-ready analytical datasets.

### Step 7

Apache Airflow automatically orchestrates Databricks jobs.

### Step 8

Power BI dashboards visualize business KPIs and analytics.

---

# 🔄 Apache Airflow Integration

Apache Airflow is used to orchestrate the complete pipeline.

## Responsibilities

- Trigger Databricks Jobs
- Schedule Pipeline Execution
- Monitor Workflow Status
- Retry Failed Jobs
- Centralize Pipeline Management

### DAG Name

```
social_media_pipeline
```

### Operator Used

```
DatabricksRunNowOperator
```

---

# ✅ Data Quality Checks

Automated validation is implemented using **Pytest**.

## Validation Rules

- Null Value Checks
- Duplicate Record Checks
- Schema Validation
- Row Count Validation
- Data Type Validation
- Primary Key Validation
- Foreign Key Validation

---

# 📊 Power BI Dashboard

The dashboard provides insights into:

## Sentiment Analysis

- Positive Tweets
- Negative Tweets
- Neutral Tweets

## Trending Analysis

- Top Hashtags
- Trending Topics

## User Analytics

- Most Active Users
- User Engagement Metrics

## Geographic Analysis

- Region-wise Sentiment
- Geographic Trend Analysis

---

# 👨‍💻 Roles & Responsibilities

### Data Ingestion

- Developed Azure Event Hub producer scripts
- Configured real-time streaming pipelines

### Bronze Layer

- Created raw Delta Lake tables
- Implemented streaming ingestion

### Silver Layer

- Developed cleansing and validation logic
- Applied business transformation rules

### Gold Layer

- Designed Star Schema
- Created Fact and Dimension tables

### Apache Airflow

- Developed orchestration DAG
- Integrated Databricks workflows

### Testing

- Implemented automated data quality validation using Pytest

### Dashboard

- Prepared curated datasets for Power BI reporting

---

# 🏆 Key Achievements

- Built an end-to-end real-time data engineering pipeline
- Implemented Medallion Architecture
- Automated workflows using Apache Airflow
- Delivered near real-time sentiment analytics
- Created business-ready reporting datasets
- Improved data quality through automated validation

---

# 🚀 Future Enhancements

- Real Twitter API Integration
- Real-Time Alerting System
- Machine Learning Sentiment Prediction
- AI-Based Trend Forecasting
- Advanced Social Media Recommendation Engine

---

# 🎯 Project Outcome

Successfully designed and implemented a scalable **Real-Time Social Media Sentiment Analysis Platform** using Azure Event Hub, Azure Databricks, Delta Lake, Apache Airflow, dbt, Power BI, and Microsoft Azure.

The solution enables organizations to ingest, process, transform, and analyze streaming social media data, delivering actionable business insights through near real-time analytics.

---

# ⭐ If you found this project useful, don't forget to Star this repository!
