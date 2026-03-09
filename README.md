# fraud-detection-big-data
# Fraud Detection using Big Data (Spark / Databricks)

## Project Overview
This project detects fraudulent credit card transactions using Big Data tools and machine learning models.

The goal is to process large-scale transaction data and identify fraud patterns using distributed computing with Apache Spark.

Fraud detection is a classic Big Data problem because of:
- Massive transaction volume
- Extreme class imbalance
- Real-world financial impact

## Dataset
Simulated credit card transaction dataset from Kaggle.

The dataset contains transaction information such as:
- Transaction amount
- Timestamp
- Merchant category
- Customer and merchant locations
- Fraud label

## Technologies
- Python
- Apache Spark
- Databricks
- Logistic Regression
- Gradient Boosted Trees

## Feature Engineering
Key engineered features include:
- Time-based features (hour, day of week, month)
- Distance between customer and merchant (Haversine distance)
- Encoded categorical variables

## Modeling
Two models were implemented:

Baseline model:
- Logistic Regression

Main model:
- Gradient Boosted Trees

## Evaluation Metrics
Because fraud data is highly imbalanced, evaluation focused on:

- ROC-AUC
- PR-AUC
- Precision
- Recall
- F1 Score
- Threshold tuning

## Business Insights
Analysis revealed that fraud risk varies across:

- Merchant categories
- Geographic locations
- Time of day
- Transaction amount

These insights can help financial institutions improve fraud monitoring strategies.

## Future Improvements
Possible extensions include:

- Real-time fraud detection using streaming pipelines (Kafka)
- Deployment of the model as an API
- Integration with real-time monitoring dashboards
