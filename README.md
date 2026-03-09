# fraud-detection-big-data
# Big Data Fraud Detection (Spark)

## Overview
This project builds a fraud detection system using large-scale credit card transaction data and Apache Spark.

The goal is to identify fraudulent transactions using distributed data processing and machine learning models.

## Dataset
Kaggle simulated credit card transaction dataset.

Two datasets (fraudTrain, fraudTest) were merged and re-split for realistic model evaluation.

##System Pipeline
Transaction Data
      ↓
Spark Data Processing
      ↓
Feature Engineering
      ↓
Machine Learning Models
(Logistic Regression / GBT)
      ↓
Model Evaluation
(ROC-AUC, PR-AUC, Precision, Recall)

## Technologies
- Python
- Apache Spark (PySpark)
- Databricks
- Logistic Regression
- Gradient Boosted Trees

## Feature Engineering
Engineered behavioral features include:

- transaction hour
- day of week
- transaction amount buckets
- spatial distance between customer and merchant

## Models
Two models were implemented:

Logistic Regression (baseline)  
Gradient Boosted Trees (main model)

## Results

| Model | ROC-AUC | PR-AUC |
|------|--------|--------|
| Logistic Regression | ~0.82 | ~0.17 |
| GBT | ~0.98 | ~0.73 |

GBT significantly improves fraud detection under severe class imbalance.

## Key Insights
- Fraud risk increases during late-night hours
- Large transactions have higher fraud probability
- Online merchant categories show higher fraud rates

## Future Work
- Real-time fraud detection pipeline
- Model deployment as API
- Streaming fraud detection with Kafka
