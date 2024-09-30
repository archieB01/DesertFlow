# DesertFlow Backend - Water Reservoir Prediction Model

# Overview
This project focuses on predicting when water levels in the Navajo Reservoir will reach critical levels, utilizing machine learning models to analyze data on storage, inflow, and release patterns. The solution is part of a larger effort to propose strategies for water conservation and management during crises.

This repository contains the backend part of the project, including data processing, model training, and prediction generation.

# Project Structure
|-- data/
|   |-- area.csv
|   |-- delta_storage.csv
|   |-- evaporation.csv
|   |-- inflow_volume.csv
|   |-- inflow.csv
|   |-- mod_unregulated_inflow_volume.csv
|   |-- mod_unregulate_inflow.csv
|   |-- release_volume.csv
|   |-- storage.csv
|   |-- total_release.csv
|   |-- unregulated_inflow_volume.csv
|   |-- unregulated_inflow.csv
|
|-- src/
|   |-- predict_sustain_model.py  # ML models for predicting storage depletion and sustainable flow behavior
|
|-- README.md

# Technologies Used
Python: Core language for backend development
Pandas: For data manipulation and analysis
NumPy: For numerical operations
Matplotlib & Seaborn: For data visualization
Scikit-learn: For machine learning model implementation

# Modeling
We implemented a Linear Regression model to predict when the water levels in the Navajo Reservoir will drop to zero. This includes:
  Model Training: 
  Using the processed dataset to train a model that predicts 'Net Storage Volume' over time.
  Prediction Analysis: 
  Estimating when the water storage will hit zero and how net flow volume behaves at this critical point.
Additional model features include:
Visualization of the predicted depletion time.
Analysis of net flow volume behavior when the reservoir is at critical storage.

# Challenges
Data Gaps: 
Some datasets had missing or inconsistent data due to irregular measurement times.
Model Accuracy: 
Other machine learning models did not provide reasonable predictions, so we focused on linear regression.
Timeline Inconsistencies: The dataset timelines were inconsistent, requiring preprocessing to ensure they aligned properly for analysis.
