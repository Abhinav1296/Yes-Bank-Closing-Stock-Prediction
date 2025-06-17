# Yes Bank Stock Price Prediction Using Machine Learning

## Overview

This project leverages advanced machine learning techniques to predict the monthly closing stock price of Yes Bank. By applying robust data preprocessing, feature engineering, and model selection strategies, the project delivers a reliable forecasting solution suitable for financial analysis and investment decision support.

---

## Table of Contents

- [Project Description](#project-description)
- [Data](#data)
- [Workflow](#workflow)
- [Results](#results)
- [How to Run](#how-to-run)
- [Key Insights](#key-insights)
- [Requirements](#requirements)
- [Future Work](#future-work)
- [License](#license)

---

## Project Description

The goal of this project is to accurately forecast Yes Bank's monthly closing stock prices using machine learning models. The workflow includes:
- Data cleaning and preprocessing
- Feature engineering (including lag features and rolling statistics)
- Dimensionality reduction
- Model selection and hyperparameter tuning (Random Forest, XGBoost, Lasso Regression)
- Model evaluation using cross-validation and test set metrics

---

## Data

- **Source:** Historical stock data for Yes Bank (2005–2020)
- **Features:** Date, Open, High, Low, Close, and engineered features (lag, rolling mean, etc.)
- **Frequency:** Monthly

---

## Workflow

1. **Data Preprocessing:**  
   - Handling missing values and outliers  
   - Scaling numerical features  
   - Encoding categorical variables (if any)

2. **Feature Engineering:**  
   - Creating lag features and rolling statistics  
   - Dimensionality reduction using PCA

3. **Modeling:**  
   - Training and tuning Random Forest, XGBoost, and Lasso Regression models  
   - Hyperparameter optimization with RandomizedSearchCV and K-Fold cross-validation

4. **Evaluation:**  
   - Comparing models using R², MAE, and RMSE on both validation and test sets  
   - Selecting the best-performing model for deployment

---

## Results

| Model                   | Test R² | CV R²    | MAE   | RMSE   |
|-------------------------|---------|----------|-------|--------|
| **XGBoost Regressor**   | 0.98    | 0.9696   | 8.11  | 11.99  |
| **Lasso Regression**    | 0.98    | 0.9622   | 8.75  | 14.24  |
| **Random Forest**       | 0.95    | 0.9413   | 14.79 | 22.09  |

- **Final Model:** XGBoost Regressor  
- **Reason:** Best balance of accuracy and generalization, with minimal overfitting and strong performance on unseen data.
