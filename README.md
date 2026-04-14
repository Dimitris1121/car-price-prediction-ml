# Car Price Prediction Using Machine Learning

## Overview
MSc Data Analytics dissertation project (University of Portsmouth, 2023).
End-to-end machine learning project predicting used car prices from 
Craigslist listings across the United States.

## Problem
The used car market involves both professionals and private sellers, 
creating significant price fluctuations. This project builds regression 
models to predict used car prices as accurately as possible, helping 
both buyers and sellers make informed decisions.

## Dataset
- **Source:** Used Cars Dataset (Kaggle) — Craigslist car listings USA
- **Original size:** 426,880 records × 26 features
- **After cleaning:** 69,951 records × 15 features
- **Target variable:** Price (USD)

## Approach
Followed the CRISP-DM methodology:
1. Business Understanding
2. Exploratory Data Analysis
3. Data Preprocessing & Cleaning
4. Model Implementation
5. Model Evaluation & Comparison

## Data Cleaning Highlights
- Dropped irrelevant columns (URLs, VIN, description etc.)
- Removed NULL values
- Removed outliers (prices > $50,000, odometer > 300,000 miles, year < 1986)
- Dropped ambiguous categorical values ('other')
- Applied Label Encoding to categorical variables

## Models Compared

| Model | R² | MAE | RMSE |
|---|---|---|---|
| **Random Forest** ⭐ | 86.60% | $2,191 | $3,808 |
| LightGBM | 83.30% | $2,752 | $4,251 |
| Decision Trees | 76.15% | $2,726 | $5,081 |
| Linear Regression | 56.64% | $5,021 | $6,850 |

## Key Findings
- Random Forest was the best performing model with R² of 86.60%
- LightGBM was a close second with strong performance
- Linear Regression significantly underperformed tree-based models
- Year and odometer were the most correlated features with price
- Ensemble and boosting methods significantly outperform linear approaches

## Tools
Python 3.10, Jupyter Notebook, pandas, numpy, 
matplotlib, seaborn, scikit-learn, LightGBM

## Files
- `Dissertation_Code.ipynb` — full analysis and modelling notebook
- `vehicles.csv` — raw dataset (download from Kaggle)

## Dataset Download
The dataset is too large for GitHub. Download it from Kaggle:
[Used Cars Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

## Academic Context
- **Degree:** MSc Data Analytics
- **Institution:** University of Portsmouth
- **Year:** 2023
- **Supervisor:** Dr. Ramazan Esmeli
