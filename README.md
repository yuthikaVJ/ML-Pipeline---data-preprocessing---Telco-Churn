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

# Telco Churn — ML Pipeline & Models

This repository implements a full ML pipeline for the Telco Customer Churn dataset: data ingestion, cleaning, feature engineering, dimensionality reduction, scaling, model training, evaluation, and result visualization.

Quick links
- Notebook workflow overview: [group_pipeline.ipynb](group_pipeline.ipynb)
- Raw dataset: [data/raw/WA_Fn-UseC_-Telco-Customer-Churn.csv](data/raw/WA_Fn-UseC_-Telco-Customer-Churn.csv)
- Final preprocessed dataset used by model notebooks: [results/outputs/final_preprocessed_telco_data_new.csv](results/outputs/final_preprocessed_telco_data_new.csv)

Repository layout
- notebooks/
  - Data preparation and EDA:  
    - [notebooks/data_cleaning_encoding.ipynb](notebooks/data_cleaning_encoding.ipynb)  
    - [notebooks/feature_engineering.ipynb](notebooks/feature_engineering.ipynb)  
    - [notebooks/outlier_removal.ipynb](notebooks/outlier_removal.ipynb)  
    - [notebooks/scaling.ipynb](notebooks/scaling.ipynb)  
    - [notebooks/dimensionality_reduction.ipynb](notebooks/dimensionality_reduction.ipynb)  
    - [notebooks/feature_selection_added.ipynb](notebooks/feature_selection_added.ipynb)
  - Model experiments (see Models section):  
    - [notebooks/models/decision_tree.ipynb](notebooks/models/decision_tree.ipynb)  
    - [notebooks/models/KNN.ipynb](notebooks/models/KNN.ipynb)  
    - [notebooks/models/Logistic Regression .ipynb](notebooks/models/Logistic Regression .ipynb)  
    - [notebooks/models/Random Forest .ipynb](notebooks/models/Random Forest .ipynb)  
    - [notebooks/models/SVM.ipynb](notebooks/models/SVM.ipynb)  
    - [notebooks/models/XGBoost .ipynb](notebooks/models/XGBoost .ipynb)
- data/
  - raw/ — original CSVs
- results/
  - eda_visualizations/
  - outputs/ — processed datasets and exported artifacts
- README.md — this file

Models (new section)
This repo contains per-model notebooks under [notebooks/models/](notebooks/models). Each notebook:
- Loads the preprocessed dataset ([results/outputs/final_preprocessed_telco_data_new.csv](results/outputs/final_preprocessed_telco_data_new.csv))
- Splits data (stratified), trains, evaluates, and visualizes results
- Produces a confusion matrix, ROC curve, feature importance (when applicable), and a brief metrics summary

Model-specific notebooks
- Decision Tree: [notebooks/models/decision_tree.ipynb](notebooks/models/decision_tree.ipynb) — baseline tree training and evaluation.
- K-Nearest Neighbors: [notebooks/models/KNN.ipynb](notebooks/models/KNN.ipynb) — tuning k and scaling effects.
- Logistic Regression: [notebooks/models/Logistic Regression .ipynb](notebooks/models/Logistic Regression .ipynb) — baseline and regularized models.
- Random Forest: [notebooks/models/Random Forest .ipynb](notebooks/models/Random Forest .ipynb) — feature importance and tuning.
- SVM: [notebooks/models/SVM.ipynb](notebooks/models/SVM.ipynb) — kernel experiments and scaling.
- XGBoost: [notebooks/models/XGBoost .ipynb](notebooks/models/XGBoost .ipynb) — baseline, GridSearchCV tuning, class-weight balancing, and cross-validation.

How to run
1. Open the repository in VS Code and launch the notebook you want from the list above.
2. Ensure the kernel has required packages (pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn).
3. Confirm the preprocessed CSV exists at [results/outputs/final_preprocessed_telco_data_new.csv](results/outputs/final_preprocessed_telco_data_new.csv) or re-run preparation notebooks starting from [notebooks/data_cleaning_encoding.ipynb](notebooks/data_cleaning_encoding.ipynb).
4. Run the notebook cells interactively. Outputs and plots will appear in the notebook and can be saved to results/.

Notes
- Notebooks assume relative paths shown in the repo. If running from a different working directory, update paths accordingly.
- The XGBoost notebook demonstrates computing scale_pos_weight from training labels and uses GridSearchCV for hyperparameter tuning; see [notebooks/models/XGBoost .ipynb](notebooks/models/XGBoost .ipynb) for details.


---





