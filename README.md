# Brent Oil Price Prediction Using Hybrid Machine Learning Models

## Project Overview

This project investigates the forecasting of Brent crude oil prices using a hybrid machine learning framework that combines traditional financial indicators, geopolitical risk measures, signal processing techniques, and machine learning algorithms.

The study aims to improve oil price forecasting performance by incorporating both market-based and external risk indicators, including volatility and geopolitical uncertainty.

---

## Research Objective

The primary objective of this study is to develop a robust forecasting framework for next-day Brent crude oil prices and evaluate whether geopolitical risk and oil market volatility provide additional predictive power beyond historical price information.

---

## Data Sources

The dataset consists of:

* Brent Crude Oil Prices (Yahoo Finance)
* CBOE Crude Oil Volatility Index (OVX) (Yahoo Finance)
* Geopolitical Risk Index (GPR)
* Geopolitical Threat Index (GPR Threat)

### References

* Caldara, D., & Iacoviello, M. (2022). Geopolitical Risk Index (GPR)
* Yahoo Finance Historical Market Data

---

## Methodology

### Data Preprocessing

The following preprocessing techniques were applied:

* Missing value handling
* Outlier treatment
* Logarithmic transformation
* Min-Max normalization
* Wavelet denoising (Daubechies DB4)

### Feature Engineering

Features generated include:

* Price lag variables (Lag1–Lag5)
* GPR lag variables
* OVX lag variables
* Exponential Moving Averages (EMA5, EMA20)

### Machine Learning Models

Three forecasting models were developed and compared:

1. XGBoost
2. LSTM (Long Short-Term Memory)
3. Hybrid Model (XGBoost + LSTM)

---

## Model Evaluation Metrics

The models were evaluated using:

* RMSE (Root Mean Square Error)
* MAE (Mean Absolute Error)
* MAPE (Mean Absolute Percentage Error)
* R² Score

In addition:

* SHAP Analysis was used for model interpretability.
* Diebold-Mariano Test was used for statistical comparison of forecast accuracy.

---

## Results

| Model        | RMSE |  MAE |  MAPE |     R² |
| ------------ | ---: | ---: | ----: | -----: |
| XGBoost      | 3.72 | 2.65 | 2.90% | 0.7872 |
| LSTM         | 4.29 | 3.40 | 3.90% | 0.6868 |
| Hybrid Model | 3.10 | 2.55 | 3.04% | 0.8356 |

### Key Findings

* The Hybrid Model achieved the best overall forecasting performance.
* XGBoost and Hybrid models significantly outperformed the standalone LSTM model.
* Historical Brent price variables were identified as the most influential predictors.
* Geopolitical and volatility indicators contributed approximately 6.81% of total model explanatory power according to SHAP analysis.

---

## Explainable AI (SHAP Analysis)

SHAP analysis was performed to quantify the contribution of each feature to model predictions.

Key observations:

* Brent price-related features dominated model decisions.
* OVX variables contributed more than GPR variables.
* External risk indicators improved model robustness during volatile market periods.

---

## Statistical Validation

The Diebold-Mariano (DM) test was conducted to determine whether differences in forecasting accuracy between models were statistically significant.

Results indicated:

* Hybrid vs XGBoost → No statistically significant difference
* Hybrid vs LSTM → Statistically significant improvement
* XGBoost vs LSTM → Statistically significant improvement

---

## Repository Structure

```text
.
├── BrentOilPricePrediction.pdf
├── requirements.txt
├── data/
│   ├── veriseti.xlsx
│   └── test_dataset.xlsx
│
├── figures/
│   ├── CorrelationHeatmap.png
│   ├── HybridModel.png
│   ├── HybridModelTest.png
│   ├── LSTMModel.png
│   ├── SHAPContributions.png
│   ├── SHAPFeaturesImportance.png
│   └── SHAPGraphs.png
│
└── notebooks/
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* TensorFlow / Keras
* SHAP
* PyWavelets
* Matplotlib
* SciPy

---

## Author

**Mustafa Enes Yeşilyurt**

Junior Data Scientist | Industrial Engineer

Sakarya University

---

## Academic Note

This repository contains the implementation, analysis, and final thesis report prepared as part of an undergraduate graduation project focused on oil price forecasting using hybrid machine learning techniques.

