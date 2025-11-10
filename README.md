# DA5401 Assignment 8: Ensemble Learning for Complex Regression

**Name:** Mahendra Kurup  
**Roll No.:** ME22B227  

## Overview

This project focuses on applying and comparing three major **ensemble learning techniques** - **Bagging**, **Boosting**, and **Stacking** - to the **Bike Sharing Demand dataset** (UCI ML Repository). Link: https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset

The task involves predicting the **total count of rented bikes (cnt)** based on various temporal and weather-related features.  

The notebook demonstrates how different ensemble strategies address the **bias–variance trade-off** and how combining diverse models can yield more accurate and robust regression performance than any single model.

## Approach

1. **Data Preparation:**  
   - Load and preprocess the **hourly bike-sharing dataset**.  
   - Drop irrelevant columns (`instant`, `dteday`, `casual`, `registered`).  
   - Apply **One-Hot Encoding** for categorical variables like `season`, `weathersit`, `mnth`, and `hr`.  
   - Split the data into **training and testing sets**.

2. **Baseline Modeling:**  
   - Train a **Decision Tree Regressor** (max depth = 6) and a **Linear Regression** model.  
   - Use **Root Mean Squared Error (RMSE)** on the test set to select the baseline model.

3. **Ensemble Techniques:**  
   - **Bagging Regressor:** Uses 50 Decision Trees to reduce variance through bootstrap aggregation.  
   - **Gradient Boosting Regressor:** Sequentially builds trees to reduce bias.  
   - **Stacking Regressor:** Combines **KNN**, **Bagging**, and **Boosting** as base learners with a **Ridge Regression** meta-learner to optimize predictions.

4. **Evaluation & Analysis:**  
   - Compute and compare **RMSE** for all models: baseline, bagging, boosting, and stacking.  
   - Discuss results in terms of **bias–variance reduction** and **model diversity**.  
   - Identify the best-performing model and interpret why it performs best.


## Requirements

To install dependencies, run:
```bash
pip install -r requirements.txt
```

## Citation
Dataset: Fanaee-T, H. (2013). Bike Sharing [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5W894.