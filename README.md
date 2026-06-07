# Credit Card Fraud Detection and Risk Analysis

# Credit Card Fraud Detection and Risk Analysis

## Dashboard Preview

![Dashboard](Project%20Dashboard%20.jpg)

## Project Overview

## Project Overview

This project focuses on analyzing credit card transaction data to identify suspicious and potentially fraudulent activities. The workflow includes data acquisition, database integration, data cleansing, exploratory analysis, and interactive dashboard development using Power BI. The objective is to uncover fraud-related patterns and provide insights that can support fraud prevention strategies.

---

## Dataset Information

**Dataset:** Credit Card Fraud Detection Dataset

**Source:** Kaggle

**File Format:** CSV

### Dataset Characteristics

* Total Transactions: 284,807
* Total Attributes: 31
* Target Variable: `Class`

  * 0 → Legitimate Transaction
  * 1 → Fraudulent Transaction
* Features:

  * PCA-transformed variables (V1–V28)
  * Transaction Time
  * Transaction Amount

### Project Goal

Analyze transaction behavior, identify fraud-related trends, and create visual reports that assist in monitoring financial risk.

---

# Data Acquisition and Preparation

### Technologies Used

* PostgreSQL
* Python (Pandas, SQLAlchemy)
* Power BI

### Dataset Collection

The transaction dataset was obtained from Kaggle and imported for further processing and analysis.

### Database Integration

The dataset was loaded into PostgreSQL using SQLAlchemy. A structured table was created with suitable numerical data types to store transaction records efficiently.

### Data Profiling

Initial database assessment was performed to evaluate data quality.

**Findings:**

* Total Records: 284,807
* Missing Values: None
* Duplicate Records: 1,854
* Feature Types: Numerical

### Data Cleaning

Data quality checks were performed in both PostgreSQL and Python.

Actions completed:

* Verified absence of null values
* Identified duplicate transactions
* Removed duplicate records from non-fraudulent transactions
* Retained all fraud-related records
* Standardized dataset structure for analysis

### Validation Process

Several validation checks ensured data consistency between PostgreSQL and Python environments.

Final cleaned dataset:

* Total Transactions: 283,745
* Legitimate Transactions: 283,253
* Fraudulent Transactions: 492

---

# Exploratory Data Analysis (EDA)

### Descriptive Statistics

Basic statistical measures were generated to understand transaction behavior.

**Highlights:**

* Average Transaction Amount: ₹88.35
* Fraud Occurrence Rate: 0.173%

### Distribution Analysis

The distribution of transaction amounts, transaction times, and fraud classes was examined using visualizations such as histograms and count plots.

**Observations:**

* Most transactions involved relatively small amounts.
* Fraud cases represented a very small portion of the dataset.

### Relationship Analysis

Comparative analysis was conducted between fraudulent and legitimate transactions.

Techniques used:

* Box Plots
* Correlation Analysis
* Feature Comparison

Several transformed variables, including V4, V10, V11, and V14, showed stronger associations with fraudulent behavior.

### Outlier Investigation

Potential anomalies were detected through visualization methods.

Rather than removing these values, they were preserved because unusual transaction patterns often indicate fraudulent activity.

---

# Power BI Dashboard Development

The cleaned dataset was imported into Power BI to create an interactive fraud-monitoring dashboard.

### Dashboard Components

#### Key Performance Indicators (KPIs)

* Total Transactions
* Fraud Percentage
* Average Transaction Amount

#### Visual Analytics

* Transaction Distribution Charts
* Fraud vs Legitimate Transaction Comparison
* Amount-Based Analysis
* Time-Based Analysis
* Interactive Filters and Slicers

### Final Dataset Summary

| Metric                  | Value   |
| ----------------------- | ------- |
| Total Records           | 283,745 |
| Legitimate Transactions | 283,253 |
| Fraudulent Transactions | 492     |
| Fraud Rate              | 0.1734% |

---

# Findings and Business Insights

### Key Observations

* Fraudulent transactions account for a very small percentage of overall activity.
* Certain PCA-derived variables exhibit stronger fraud-related signals.
* Fraud activity frequently appears within specific transaction amount ranges and time windows.
* The dataset demonstrates a significant class imbalance, making fraud detection a challenging task.

### Business Impact

Even low-value fraudulent transactions can generate substantial cumulative financial losses. Early identification of suspicious behavior is therefore essential for reducing risk exposure.

---

# Recommendations

* Implement anomaly detection systems using highly correlated fraud indicators.
* Increase monitoring for transactions exhibiting known fraud characteristics.
* Utilize real-time dashboard reporting for continuous fraud surveillance.
* Refresh analytical models regularly as new transaction data becomes available.
* Establish automated alert mechanisms for high-risk transactions.

---

# Future Enhancements

* Develop machine learning models for predictive fraud detection.
* Enable automated Power BI data refresh workflows.
* Integrate the solution with live transaction streams for real-time monitoring.
* Explore advanced classification techniques to improve fraud detection accuracy.

---

# Repository Contents

| File                                    | Description                               |
| --------------------------------------- | ----------------------------------------- |
| creditcard_project.ipynb                | Data exploration and analysis notebook    |
| CC_Project.sql                          | PostgreSQL scripts used for data handling |
| CreditCardFraudDetection_Dashboard.pbix | Interactive Power BI dashboard            |
| Project Dashboard.jpg                   | Dashboard snapshot                        |
| creditcard_project.pdf                  | Detailed project report                   |
| README.md                               | Project documentation                     |

---

## Conclusion

This project demonstrates an end-to-end fraud analytics workflow, covering data preparation, validation, exploratory analysis, and dashboard reporting. The insights generated can support financial institutions in strengthening fraud monitoring processes and improving risk management capabilities.



Author
Sankalp
