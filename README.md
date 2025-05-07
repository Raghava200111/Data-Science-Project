# Data-Science-Project
# MSc Data Science Final Project  
*Module:* 7PAM2002  
*Programme:* MSc Data Science  
*University:* University of Hertfordshire  
*Department:* Physics, Astronomy and Mathematics  

## Project Title  
*Forecasting International Stock Market Trends: A Cross-Country Analysis Using SARIMA and Prophet*

*Student Name:* Veera Raghava Reddy Kudumula  
*Student SRN:* 23013925  
*Supervisor:* Dr. Ralf Napiwotzki  
*Submission Date:* 29 April 2025  
*Project Word Count:* 5,000  
*GitHub Repository:* [https://github.com/Raghava200111/Data-Science-Project](https://github.com/Raghava200111/Data-Science-Project)

---

## Overview

This project aims to evaluate and compare the forecasting performance of two time series models: SARIMA (Seasonal Autoregressive Integrated Moving Average) and Facebook Prophet. The goal is to determine their relative effectiveness in predicting stock market trends across different national economies, both developed and emerging. By applying these models to a historical dataset of stock indices from the World Bank, the study identifies which model is better suited for specific market conditions.

---

## Data Description

- *Source:* World Bank Open Data  
- *Data Range:* 1995 to 2025  
- *Frequency:* Monthly  
- *Countries Analyzed:*  
  - Singapore  
  - Venezuela (RB)  
  - Egypt (Arab Rep.)  
  - Indonesia  
  - Bosnia and Herzegovina  
- *Key Features:* Stock market index values, market capitalization metrics, time indicators  

The dataset is publicly available and contains no personal or sensitive information.

---

## Methodology

The methodology consisted of the following steps:

### Data Preparation
- Data cleaning: forward-fill and mean imputation for missing values
- Outlier detection and removal using z-scores
- Duplicate removal
- Data transformation: log transformation, robust scaling, and power transformation
- Feature engineering: computed moving averages and volatility indicators

### Forecasting Models
- *SARIMA*  
  Used for modeling seasonality and trends with structured, stationary data.
- *Prophet*  
  Designed to capture complex seasonality, outliers, and trend changes. Suitable for volatile and irregular data.

### Model Evaluation
Models were compared using:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)

Evaluation was based on a 12-month backtesting period. A 60-month (five-year) forecast was also generated.

---

## Results Summary

| Country                | Best Model | Key Observations |
|------------------------|------------|------------------|
| Singapore              | SARIMA     | Captured seasonality accurately with low error |
| Venezuela (RB)         | SARIMA     | Provided stable, conservative forecasts in a volatile market |
| Egypt (Arab Rep.)      | Neither    | High volatility and sparse data led to poor performance in both models |
| Indonesia              | Prophet    | Captured non-linear growth trends more effectively |
| Bosnia and Herzegovina | SARIMA     | Demonstrated consistency and accuracy in declining trend forecasting |

Prophet tended to perform better in markets with smooth non-linear growth, whereas SARIMA excelled in stable, seasonal environments.

---

## Repository Structure
---

## Ethical Considerations

- No human participants were involved in the study.
- No personal or identifiable data was used.
- All data used is publicly available and covered by the World Bank Open Data License.
- Ethical approval from the University of Hertfordshire was not required due to the nature of the data.

---

## Key Contributions

- Demonstrated the effectiveness of SARIMA in stable markets and Prophet in growth-based environments.
- Highlighted challenges in forecasting in volatile economies like Egypt.
- Provided a reproducible and transparent pipeline for stock market trend forecasting.
- Offered practical implications for financial analysts, investors, and policymakers.

---

## Limitations and Future Work

- Only univariate time series models were used; incorporating macroeconomic variables could enhance performance.
- SARIMA model parameters were not exhaustively optimized.
- Future research may explore hybrid models or use deep learning techniques such as LSTM or CNN for improved forecasting.
- Shorter forecast horizons may be more effective in highly volatile environments.

---

## Software and Libraries

- Python 3.9+
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- prophet (fbprophet)
- scikit-learn

To install all dependencies, use:

```bash
pip install -r requirements.txt
