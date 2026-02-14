# 🔋 EV Battery Capacity Degradation Prediction

Machine Learning | Linear Regression | Ridge | Lasso | ElasticNet | Cross Validation

---

## 📌 Project Overview

This project focuses on predicting **battery capacity degradation (%)** in Electric Vehicles (EVs) using operational usage factors.

The dataset contains 5,000 AI-generated EV usage records simulating realistic battery degradation curves influenced by:

- Charge Cycles
- Fast Charging Frequency
- Average Temperature
- Driving Aggression Index

The objective was to build and compare multiple linear regression models and evaluate their performance using cross-validation and regularization techniques.

---

# ⭐ STAR Framework

## 🟢 Situation

Battery degradation is one of the biggest challenges in EV lifecycle management.  
Manufacturers and fleet operators need reliable predictive models to estimate battery health based on usage behavior and environmental conditions.

However:
- Degradation patterns can be influenced by multiple correlated factors.
- Overfitting can occur without proper regularization.
- Model stability is critical for deployment in real-world predictive maintenance systems.

---

## 🟡 Task

Develop a regression-based machine learning solution to:

1. Analyze EV battery degradation patterns.
2. Build a predictive model using linear regression.
3. Compare standard Linear Regression with:
   - Ridge Regression
   - Lasso Regression
   - ElasticNet Regression
4. Apply cross-validation and hyperparameter tuning.
5. Evaluate model performance using robust metrics.

---

## 🔵 Action

The following steps were performed:

### 1️⃣ Data Understanding & EDA
- Checked shape, summary statistics, and distributions
- Visualized feature relationships
- Correlation analysis

### 2️⃣ Feature Engineering
- Feature scaling using StandardScaler
- Train-test split (80/20)
- 5-fold cross-validation

### 3️⃣ Model Development
Implemented and compared:

- Linear Regression
- Ridge Regression (L2 regularization)
- Lasso Regression (L1 regularization)
- ElasticNet (L1 + L2)

Hyperparameters were optimized using GridSearchCV.

### 4️⃣ Evaluation Metrics
Models were evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## 🟣 Results

| Model        | R² Score | MAE  | RMSE |
|--------------|----------|------|------|
| Linear       | 0.75356  | 1.3304 | 1.6627 |
| Ridge        | 0.75357  | 1.3303 | 1.6626 |
| Lasso        | 0.75358  | 1.3303 | 1.6626 |
| ElasticNet   | **0.75377** | **1.3299** | **1.6619** |

### 🔍 Key Insights

- Approximately 75% of degradation variance is explained by usage features.
- Regularization slightly improved generalization.
- ElasticNet delivered the best overall performance.
- The relationship between usage factors and degradation is largely linear.

---

# 🧠 Technical Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

# 📊 Business Impact

This model can be used for:

- EV battery health prediction
- Warranty risk estimation
- Fleet maintenance optimization
- Predictive maintenance systems
- Battery lifecycle planning

---

# 📂 Dataset

The dataset contains 5,000 synthetic EV usage records designed to simulate real-world degradation patterns.

Columns:
- Charge_Cycles
- Fast_Charging_Frequency_%
- Avg_Temperature_C
- Driving_Aggression_Index
- Battery_Degradation_%

---

# 🚀 Future Improvements

- Add time-series degradation tracking
- Deploy via Streamlit
- Add SHAP interpretability
- Compare with tree-based models (XGBoost, Random Forest)
- Incorporate battery chemistry variations (LFP vs NMC)
