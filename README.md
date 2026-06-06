# Walmart Weekly Sales Forecasting

## Project Overview
End-to-end data science capstone project analyzing and forecasting 
weekly sales across 45 Walmart stores using statistical analysis 
and time series modeling.

## Problem Statement
Walmart faces inventory management challenges across multiple outlets. 
This project provides insights into sales drivers and forecasts 
the next 12 weeks of sales per store.

## Dataset
- 6,435 rows, 8 columns
- Features: Store, Date, Weekly_Sales, Holiday_Flag, 
  Temperature, Fuel_Price, CPI, Unemployment

## Key Findings
- Stores 38 and 44 are most negatively impacted by unemployment
- Clear holiday seasonality spike every November-December
- Temperature and CPI show negligible effect on sales (correlation < 0.1)
- Store 20 is the top performer (~$301M total sales)
- Store 33 is the worst performer (~$37M) — 8x gap from best

## Forecasting Model
- Model: SARIMA(1,0,1)(1,1,0,52)
- Parameters justified using ADF test and ACF/PACF analysis
- Train/Test split: last 12 weeks as test set

## Model Performance (MAPE)
| Store | MAPE |
|-------|------|
| Store 1 | 2.54% |
| Store 2 | 3.48% |
| Store 20 | 3.07% |
| Store 33 | 6.83% |
| Store 44 | 3.74% |

All stores achieved MAPE under 7%, well within the 
acceptable retail forecasting threshold of 20%.

## Tech Stack
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Statsmodels (SARIMA, seasonal decompose, ADF test)
- Jupyter Notebook

## Project Structure

walmart-forecasting/
│
├── walmart_capstone.ipynb   # Main notebook
├── walmart.csv  # Dataset
└── README.md

## Author
Bhargavi Chakrapani | Data Scientist | Hyderabad
[https://www.linkedin.com/in/bhargavi-c-a33847293/]
