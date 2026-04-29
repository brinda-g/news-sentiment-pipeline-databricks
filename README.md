# 📰 News Sentiment Intelligence Pipeline

An end-to-end ETL data pipeline built on **Apache Spark** and **Databricks** that ingests real financial news headlines, applies AI-powered NLP sentiment analysis, and loads results into **Delta Lake** for business intelligence reporting.

---

## 🧠 Project Overview

This project was developed as part of **COSC2637 Big Data Processing** at **RMIT University**. It demonstrates a real-world big data pipeline using industry-standard tools and techniques.

The pipeline answers a key business question:

> *"What is the overall sentiment of today's financial news — and which outlets report most positively or negatively?"*

---

## 🏗️ Pipeline Architecture

**Extract → Transform → Load (ETL)**

- **Extract** — Load raw financial news headlines into Apache Spark
- **Transform** — Apply AI sentiment scoring using VADER NLP via Spark UDFs
- **Load** — Save results into Delta Lake tables for BI reporting

---

## ⚙️ Tech Stack

| Tool | Purpose |
|---|---|
| **Databricks** | Cloud platform for running the pipeline |
| **Apache Spark** | Distributed big data processing engine |
| **PySpark** | Python API for Spark |
| **VADER NLP** | AI sentiment scoring library |
| **Delta Lake** | Enterprise-grade storage layer |
| **Python** | Primary programming language |

---

## 📊 Pipeline Stages

### 1. Extract
- Loads 20 real financial news headlines from major outlets
- Sources include Reuters, Bloomberg, CNBC and Financial Times
- Creates a Spark DataFrame for distributed processing

### 2. Transform
- Applies VADER NLP sentiment scoring via Spark UDFs
- Classifies each headline as Positive, Negative or Neutral
- Assigns a confidence score between -1.0 and 1.0
- Aggregates sentiment breakdown by news source

### 3. Load
- Saves scored headlines to Delta Lake table: financial_news_sentiment
- Saves source aggregations to Delta Lake table: sentiment_by_source
- Generates final business intelligence summary report

---

## 📈 Sample Output

- Total headlines analysed: 20
- Positive sentiment: 11 (55%)
- Negative sentiment: 7 (35%)
- Neutral sentiment: 2 (10%)
- Most positive outlet: CNBC (avg score: 0.1603)
- Most negative outlet: Reuters (avg score: -0.0337)
- Overall market mood: BULLISH 📈
- Pipeline Status: SUCCESS ✅
- Storage Layer: Delta Lake
- Processing Engine: Apache Spark

---

## 🚀 How to Run

1. Create a free Databricks account at databricks.com
2. Import News_Sentiment_Pipeline.ipynb into your Databricks workspace
3. Run all cells in order using Shift + Enter

---

## 👩‍💻 Author

**Brinda Gandhi Rajan**
Master of Data Science — RMIT University
COSC2637 Big Data Processing
