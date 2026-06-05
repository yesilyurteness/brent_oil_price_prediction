# Brent Oil Price Forecasting Using Hybrid Machine Learning Models

## Overview

This project presents a hybrid machine learning framework for forecasting Brent crude oil prices by combining traditional financial indicators, geopolitical risk measures, advanced signal processing techniques, and machine learning algorithms.

The study investigates the predictive power of:

* Brent Crude Oil Prices
* CBOE Crude Oil Volatility Index (OVX)
* Geopolitical Risk Index (GPR)
* Geopolitical Threat Index (GPR Threat)

The proposed framework integrates Wavelet Denoising, Feature Engineering, XGBoost, LSTM, SHAP Explainability Analysis, and Diebold-Mariano statistical testing to improve forecasting performance and model interpretability.

---

## Methodology

### 1. Data Collection

Data sources used in this study:

* Brent Crude Oil Prices (Yahoo Finance)
* OVX Index (Yahoo Finance)
* Geopolitical Risk Index (GPR)
* Geopolitical Threat Index (GPR Threat)

### 2. Data Preprocessing

The following preprocessing techniques were applied:

* Missing value handling
* Wavelet Denoising (DB4)
* Logarithmic Transformation
* Winsorization
* Min-Max Scaling

### 3. Feature Engineering

Features generated include:

* Lag Features (1–5 days)
* Exponential Moving Averages (EMA5, EMA20)
* Volatility-based indicators
* Geopolitical risk indicators

### 4. Machine Learning Models

The following forecasting models were developed and compared:

* XGBoost
* Long Short-Term Memory (LSTM)
* Hybrid Model (XGBoost + LSTM)

### 5. Model Evaluation

Performance was evaluated using:

* RMSE
* MAE
* MAPE
* R² Score

Additionally:

* SHAP Analysis was used for model interpretability.
* Diebold-Mariano Test was used for statistical comparison of forecasting accuracy.

---

## Results

| Model        | RMSE |  MAE |  MAPE |     R² |
| ------------ | ---: | ---: | ----: | -----: |
| XGBoost      | 3.72 | 2.65 | 2.90% | 0.7872 |
| LSTM         | 4.29 | 3.40 | 3.90% | 0.6868 |
| Hybrid Model | 3.10 | 2.55 | 3.04% | 0.8356 |

The Hybrid Model achieved the highest overall forecasting performance.

Diebold-Mariano test results showed that both Hybrid and XGBoost models significantly outperformed the LSTM model, while the performance difference between Hybrid and XGBoost was not statistically significant.

---

## Explainable AI (SHAP Analysis)

SHAP analysis revealed that:

* Historical Brent oil price variables were the dominant predictors.
* Volatility and geopolitical risk variables contributed approximately 6.81% of the overall model decision process.
* OVX variables provided higher explanatory power than GPR variables.

---

## Repository Structure

```text
.
├── BrentOilPricePrediction.pdf
├── requirements.txt
├── data/
├── figures/
└── notebooks/
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Author

**Mustafa Enes Yeşilyurt**

Junior Data Scientist | Industrial Engineer



---

## Academic Project

This repository contains the implementation and thesis report prepared as part of an undergraduate graduation project.
