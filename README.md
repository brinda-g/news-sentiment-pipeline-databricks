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
- Saves scored headlines to Delta Lake table: `financial_news_sentiment`
- Saves source aggregations to Delta Lake table: `sentiment_by_source`
- Generates final business intelligence summary report

---
## 👩‍💻 Author

**Brinda Gandhi**  
Master of Data Science — RMIT University  
COSC2637 Big Data Processing
