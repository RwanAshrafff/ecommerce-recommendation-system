# E-Commerce Product Recommendation System

An end-to-end E-Commerce Analytics & Recommendation System that integrates Data Engineering, Machine Learning, Association Rule Mining, Customer Segmentation, and Business Intelligence into a single pipeline.

## Features

- PostgreSQL Data Warehouse
- Medallion Architecture (Bronze → Silver → Gold)
- Star Schema Design
- FP-Growth Association Rule Mining
- Customer Segmentation using RFM + K-Means
- Customer Value Prediction using Logistic Regression
- Interactive Power BI Dashboard
- Geographic Sales Analytics
- Real-time BI Reporting

---

# Tech Stack

## Languages
- Python
- SQL

## Data Engineering
- PostgreSQL
- pgAdmin 4

## Machine Learning
- Pandas
- NumPy
- Scikit-learn
- mlxtend

## Visualization
- Power BI

---

# Dataset

- UCI Online Retail Dataset
- ISO Country Mapping Dataset
- Product Category Mapping Dataset

---

# Data Warehouse Architecture

## Bronze Layer
Raw data ingestion from CSV files.

## Silver Layer
Data cleaning and preprocessing:
- Removed invalid quantities/prices
- Parsed timestamps
- Handled missing values
- Preserved cancellation analytics

## Gold Layer
Star Schema including:

### Fact Table
- fact_sales

### Dimension Tables
- dim_customer
- dim_product
- dim_country
- dim_date

---

# Machine Learning Models

## 1. Association Rule Mining

### Algorithm
- FP-Growth

### Thresholds
- Minimum Support = 0.01
- Minimum Confidence = 0.5
- Minimum Lift = 1.5

### Results
- 1,902 frequent itemsets discovered
- Strong cross-selling opportunities identified

---

## 2. Customer Value Prediction

### Features
- Recency
- Frequency
- Monetary
- Average Order Value

### Model
- Logistic Regression

### Performance

| Metric | Value |
|---|---|
| Accuracy | 93.55% |
| Precision | 96.00% |
| Recall | 87.52% |
| F1 Score | 91.57% |
| AUC | 0.9885 |

---

## 3. Customer Segmentation

### Techniques
- RFM Analysis
- PCA
- MiniBatch K-Means

### Clusters
- VIP Customers
- Inactive/Lost Customers

### Evaluation
- Silhouette Score > 0.70

---

# Power BI Dashboard

The dashboard contains:

## Home Dashboard
- Revenue KPIs
- Monthly Sales Trends
- Product Analysis
- Geographic Insights

## Customer Insights
- Customer Segmentation
- Spending Analysis
- RFM Analytics

## Country Insights
- Regional Revenue Analysis
- Market Expansion Opportunities

---

# Project Structure

```bash
├── Dashboard.pbix
├── Models.ipynb
├── Paper.pdf
├── datasets/
├── sql/
├── visuals/
└── README.md
