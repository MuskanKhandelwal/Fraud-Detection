# Fraud-Detection

## Overview

This project aims to detect fraud in financial transactions using various data preprocessing techniques and machine learning algorithms. The dataset used contains information about different transactions and related attributes.

## Data Preprocessing

1. **Handling Missing Values:**
   - Missing values are filled with the mean of the respective columns.

2. **Data Imbalance:**
   - The data is imbalanced, as observed from both the graphs and the percentage of fraud vs. non-fraud transactions. But didn not used SMOTE as it's not the best choice 
     everytime.

3. **Encoding Methods:**
   - **One-Hot Encoding for Non-Ordinal Categories:**
     1. `transactionType`
     2. `transaction_device`
     3. `AccountType_sender`
     4. `AccountType_receiver`
   - **Label Encoding for Ordinal Categories:**
     1. `TransactionFrequency_sender`
     2. `TransactionFrequency_receiver`

## Machine Learning Models

The notebook includes the implementation of various machine learning models to predict fraudulent transactions. These models include:
1. **Random Forest:**
   - An ensemble learning method that constructs multiple decision trees during training.
   - Outputs the mode of the classes (classification) or mean prediction (regression) of the individual trees.
   - Effective in handling imbalanced datasets and reducing overfitting.

2. **XGBoost:**
   - An optimized gradient boosting library designed to be highly efficient, flexible, and portable.
   - Implements machine learning algorithms under the Gradient Boosting framework.
   - Known for its speed and performance, especially in structured/tabular data.

3. **CatBoost:**
   - A gradient boosting algorithm that handles categorical features automatically.
   - Provides state-of-the-art results for many machine learning tasks without extensive hyperparameter tuning.
   - Known for its fast training speed and high accuracy, even with default parameters.


## Results

1. **Random Forest:**
   - ROC AUC: 0.9188
   - AUPRC: 0.8362

2. **XGBoost:**
   - ROC AUC: 0.9984
   - AUPRC: 0.9744

3. **CatBoost:**
   - ROC AUC: 0.9352

