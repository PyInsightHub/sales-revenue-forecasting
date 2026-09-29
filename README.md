# 🍔 **ꜱᴀʟᴇꜱ ᴅᴀᴛᴀ ᴀɴᴀʟʏꜱɪꜱ & ʀᴇᴠᴇɴᴜᴇ ꜰᴏʀᴇᴄᴀꜱᴛɪɴɢ**


>An end-to-end data science project analyzing fast-food restaurant sales across five European cities — covering data cleaning, exploratory analysis, feature engineering, machine learning-based revenue forecasting, model explainability, and a deployable Streamlit dashboard.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)



![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B.svg)



![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E.svg)



![License](https://img.shields.io/badge/License-MIT-green.svg)





---

## 📊 Project Overview

This project analyzes transactional sales data (orders, products, pricing, purchase channels, payment methods, managers, and cities) to uncover business insights and build a predictive model for daily revenue forecasting.

**Key objectives:**
- Clean and validate messy real-world transactional data
- Perform in-depth exploratory data analysis (EDA)
- Engineer time-based and categorical features
- Train and tune regression models to forecast daily revenue
- Explain model predictions using SHAP
- Quantify forecast uncertainty with prediction intervals
- Deploy results via an interactive Streamlit dashboard

---

## 🗂️ Dataset

The dataset contains order-level sales records with the following fields:

| Column | Description |
|---|---|
| `Order ID` | Unique transaction identifier |
| `Date` | Order date |
| `Product` | Item category (Burgers, Fries, Beverages, etc.) |
| `Price` | Unit price |
| `Quantity` | Units sold |
| `Purchase Type` | Online, In-store, or Drive-thru |
| `Payment Method` | Credit Card, Cash, or Gift Card |
| `Manager` | Store manager on record |
| `City` | Store location (London, Madrid, Lisbon, Berlin, Paris) |

---

## 🔍 Workflow

### 1. Data Import & Cleaning
- Null value and duplicate checks
- Outlier detection via IQR on price/quantity
- Whitespace normalization on categorical fields (manager names, cities)
- Data type validation and correction

### 2. Exploratory Data Analysis (EDA)
- Revenue breakdowns by product, city, manager, purchase channel, and payment method
- Time-series trends: daily, monthly, and day-of-week revenue patterns
- Month-over-month growth analysis
- Correlation analysis across numeric features
- Interactive Plotly visualizations (3D scatter, heatmaps, violin plots)

### 3. Feature Engineering
- Calendar features: month, quarter, day of week, weekend flag
- Lag features (1, 7, 14 days) and rolling statistics (mean, std) for time-series modeling
- Revenue share and cumulative contribution metrics

### 4. Machine Learning
- **Models:** Random Forest Regressor, Gradient Boosting Regressor (benchmarked against a seasonal naive baseline)
- **Validation:** Time-series cross-validation (`TimeSeriesSplit`) to respect temporal order
- **Tuning:** `RandomizedSearchCV` hyperparameter optimization
- **Metrics:** MAE, RMSE, R²
- **Explainability:** SHAP values (beeswarm, waterfall, dependence plots) for feature-level interpretation
- **Uncertainty quantification:** Empirical prediction intervals via residual calibration

### 5. Deployment
- Best model serialized with `joblib`
- Interactive dashboard built with **Streamlit**
- Exportable HTML forecasting dashboard (Plotly)

---

## 🛠️ Tech Stack

- **Language:** Python 3.10+
- **Data Processing:** pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Machine Learning:** scikit-learn, SHAP
- **Deployment:** Streamlit, joblib

---

## 📁 Project Structure
