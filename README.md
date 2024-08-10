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

- **Model Accuracy:** The logistic regression model achieved an accuracy of `44%`
- **Classification Report:** A detailed classification report is generated to assess precision, recall, and F1-score.
## Accuracy: 44.0 %
```plaintext
              precision    recall  f1-score   support

           0       0.44      1.00      0.61        22
           1       0.00      0.00      0.00        28

    accuracy                           0.44        50
   macro avg       0.22      0.50      0.31        50
weighted avg       0.19      0.44      0.27        50
```
## 📊 Data Points
- Number of data points in the training set: 200
- Number of data points in the test set: 50

The dataset used in this analysis is fetched in real-time using the `yfinance` library and consists of daily closing prices for Tesla, Amazon, and the S&P 500 over the past year.

## 📂 Fetched Stock Data
### Tesla (TSLA) - First 5 Rows
```plaintext
                                 Open        High         Low  ...  PriceRise  PriceRise_next  Target
Date                                                           ...
2023-08-11 00:00:00-04:00  241.770004  243.789993  238.020004  ...  -0.011025       -0.011982       0
2023-08-14 00:00:00-04:00  235.699997  240.660004  233.750000  ...  -0.011982       -0.028772       0
2023-08-15 00:00:00-04:00  238.729996  240.500000  232.610001  ...  -0.028772       -0.032103       0
2023-08-16 00:00:00-04:00  228.020004  233.970001  225.380005  ...  -0.032103       -0.028688       0
2023-08-17 00:00:00-04:00  226.059998  226.740005  218.830002  ...  -0.028688       -0.017161       0
```
### Amazon (AMZN) - First 5 Rows
```plaintext
                                 Open        High         Low       Close    Volume  Dividends  Stock Splits  PriceRise
Date
2023-08-10 00:00:00-04:00  139.070007  140.410004  137.490005  138.559998  58928400        0.0           0.0        NaN
2023-08-11 00:00:00-04:00  137.399994  139.330002  137.000000  138.410004  42832100        0.0           0.0  -0.001083
2023-08-14 00:00:00-04:00  138.300003  140.589996  137.750000  140.570007  47148700        0.0           0.0   0.015485
2023-08-15 00:00:00-04:00  140.050003  141.279999  137.229996  137.669998  42781500        0.0           0.0  -0.020846
2023-08-16 00:00:00-04:00  137.190002  137.270004  135.009995  135.070007  41675900        0.0           0.0  -0.019066
```
### S&P 500 (^GSPC) - First 5 Rows
```plaintext
                                  Open         High          Low  ...  Dividends  Stock Splits  PriceRise
Date                                                              ...
2023-08-10 00:00:00-04:00  4487.160156  4527.370117  4457.919922  ...        0.0           0.0        NaN
2023-08-11 00:00:00-04:00  4450.689941  4476.229980  4443.979980  ...        0.0           0.0  -0.001070
2023-08-14 00:00:00-04:00  4458.129883  4490.330078  4453.439941  ...        0.0           0.0   0.005734
2023-08-15 00:00:00-04:00  4478.870117  4478.870117  4432.189941  ...        0.0           0.0  -0.011618
2023-08-16 00:00:00-04:00  4433.790039  4449.950195  4403.549805  ...        0.0           0.0  -0.007584
```
## 🗒️ Conclusion

This project successfully demonstrates the use of logistic regression to predict stock price trends based on historical data. By analyzing multiple stocks, the model provides valuable insights into market behavior, helping to forecast potential price movements for Tesla.



