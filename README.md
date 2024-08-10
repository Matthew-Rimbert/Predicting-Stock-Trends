# 📈 Predicting Stock Trends
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.2.4+-red.svg)
![NumPy](https://img.shields.io/badge/NumPy-1.19.2+-orange.svg)
![SciKit-Learn](https://img.shields.io/badge/SciKit--Learn-0.23.2+-yellow.svg)
![yFinance](https://img.shields.io/badge/yFinance-0.1.63+-green.svg)
![Yahoo Finance](https://img.shields.io/badge/Data-Yahoo%20Finance-yellow.svg)

## 🎯 Project Overview

This project focuses on predicting stock price trends using machine learning, specifically a logistic regression model. The analysis includes multiple stocks, such as Tesla (TSLA), Amazon (AMZN), and the S&P 500 (^GSPC). The goal is to predict whether the TSLA stock price will rise the next day based on historical data.

## 📝 Purpose

- Predict stock price trends using machine learning techniques.
- Analyze multiple stocks (Tesla, Amazon, and S&P 500) to improve prediction accuracy.

## 📊 Scope of Work

1. **Fetch Historical Stock Data:** 
   - Data for Tesla (TSLA), Amazon (AMZN), and S&P 500 (^GSPC) was collected using the `yfinance` library.
  
2. **Calculate Price Changes and Other Relevant Features:** 
   - Daily price rise (log returns) was calculated for each stock.
   - The price rise data was shifted to align with the target prediction day.
  
3. **Train and Evaluate a Logistic Regression Model:**
   - A logistic regression model was trained on the processed data.
   - The model was evaluated using accuracy and classification metrics.

## 🚀 Methodology

### 1. Importing Necessary Libraries

```python
import yfinance as yf
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn import metrics
```

## 📈 Results

- **Model Accuracy:** The logistic regression model achieved an accuracy of `X%` (replace with your actual result) on the test set.
- **Classification Report:** A detailed classification report is generated to assess precision, recall, and F1-score.

## 📂 Dataset

The dataset used in this analysis is fetched in real-time using the `yfinance` library and consists of daily closing prices for Tesla, Amazon, and the S&P 500 over the past year.

## 🗒️ Conclusion

This project successfully demonstrates the use of logistic regression to predict stock price trends based on historical data. By analyzing multiple stocks, the model provides valuable insights into market behavior, helping to forecast potential price movements for Tesla.



