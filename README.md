# Renewable Energy Power Plant Classifier

Machine learning project that predicts whether a power plant is **renewable or non-renewable** based on operational and geographic features.

## Overview
This project builds a binary classification model that determines whether a power plant uses a renewable energy source.  
The target variable `is_renewable` is derived from the `primary_fuel` column in the **Global Power Plant Database**. :contentReference[oaicite:0]{index=0}

The goal is to explore how machine learning can help classify energy infrastructure using publicly available data.

## Dataset
Source: Global Power Plant Database (WRI)

After preprocessing the dataset contains ~34k power plants with features such as:
- plant capacity
- plant age
- geographic coordinates
- country

Example features used in the model:
- `log1p_capacity`
- `age`
- `latitude`
- `longitude`
- `country` :contentReference[oaicite:1]{index=1}

## Methods
The workflow includes:

1. Exploratory Data Analysis (EDA)
2. Data preprocessing and feature engineering
3. Handling missing values and categorical variables
4. Train/test split with stratification
5. Model training and hyperparameter tuning

Models tested:
- Logistic Regression
- Random Forest

Hyperparameters were optimized using **GridSearchCV and RandomizedSearchCV**. :contentReference[oaicite:2]{index=2}

## Results
The best model was **Random Forest**.

Performance on the test dataset:
- Accuracy ≈ 0.93
- ROC AUC ≈ 0.98
- Weighted F1 ≈ 0.93 :contentReference[oaicite:3]{index=3}

The model significantly outperformed both the baseline classifier and logistic regression.

## Key Insights
The most important predictors include:
- plant age
- power capacity
- geographic location
- country of operation :contentReference[oaicite:4]{index=4}

These factors align with real-world energy production patterns.

## Tech Stack
- Python
- Pandas
- Scikit-learn
- Imbalanced-learn
- Matplotlib / Seaborn

## Author
Veronika Nozdrenkova
