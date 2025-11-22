# ML-Pipeline---data-preprocessing---Telco-Churn


# Customer Churn Prediction

## Project Overview 

This project focuses on preprocessing the Telco Customer Churn Dataset to prepare it for machine learning modeling.
The objective is to clean, transform, and enhance the dataset using different preprocessing techniques such as missing value handling, encoding, scaling, outlier removal, feature engineering, feature selection, and dimensionality reduction.
Each preprocessing technique was handled by one group member, and the results were integrated into a single pipeline.


---






## 📊 Dataset Information

* **Name of Dataset**: Telco Customer Churn
* **Source**: [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
* **Number of Records**: 7043 rows
* **Number of Features (after preprocessing)**: 10 columns
* **Target Variable**: `Churn` (Yes/No → encoded as 1/0)

## 🔧 Data Preprocessing Steps

1. **Handling Missing Values** – Cleaned and imputed missing data.
2. **Encoding Categorical Variables** – Converted categorical features into numerical format.
3. **Scaling Numerical Features** – Standardized numerical columns for better model performance.
4. **Outlier Removal** – Detected and removed extreme values.
5. **Feature Engineering** – Created new features:

   * `services_count`
   * `avg_charge_per_month`
   * `tenure_group`
6. **Feature Selection** – Selected the most relevant features for prediction.
7. **Dimensionality Reduction** – Reduced data complexity while retaining important information.

## 🎯 Objective

To predict customer churn (whether a customer will leave or stay) based on service usage patterns and demographic details.

## 📌 Notes

* Target variable (`Churn`) is encoded as binary (1 = Yes, 0 = No).
* Data is preprocessed and ready for modeling.


---





