# 🚗 Vehicle Selling Price Prediction

> A machine learning regression model that predicts vehicle selling prices using historical sales transaction data — built to support automotive dealerships, auction platforms, and valuation businesses with accurate, data-driven pricing.

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

---

## 📌 Overview

Automotive dealerships, vehicle auction platforms, banks, and insurance companies face real challenges in determining accurate resale prices — manual valuation is time-consuming, inconsistent, and dependent on human expertise.

This project solves that problem with a regression-based ML model that learns from historical vehicle sales data — analyzing specifications, condition, mileage, market value (MMR), and transaction details — to estimate selling price accurately.

---

## 🎯 Objectives

- Build a predictive model capable of estimating vehicle selling prices
- Identify the most influential factors affecting vehicle prices
- Improve pricing strategies for dealerships and automotive businesses
- Support market trend analysis and data-driven decision-making

---

## 🗂️ Dataset

| Feature | Description |
|---|---|
| `make`, `model`, `trim`, `body` | Vehicle identity & specifications |
| `transmission` | Automatic / Manual |
| `condition` | Vehicle condition rating |
| `odometer` | Mileage reading |
| `color`, `interior` | Exterior & interior color |
| `seller` | Selling dealer/entity |
| `mmr` | Manheim Market Report — benchmark market value |
| `sellingprice` | 🎯 Target variable — actual selling price |

*(Columns `vin`, `saledate`, and `state` were dropped — not predictive of price.)*

---

## 🔄 ML Pipeline

```
Understand Problem → Clean Data → Handle Null Values → Handle Outliers
   → Encoding → Scaling → Train-Test Split → Choose Algorithm
   → Train Model → Predict → Evaluate → Check Overfitting → Improve Model
```

---

## ⚙️ What Was Done

1. **Data Cleaning** — Dropped irrelevant columns, filled missing values using statistically appropriate defaults (mode/median)
2. **Exploratory Data Analysis** — Distribution plots, boxplots, and skewness checks on `sellingprice`, `mmr`, `odometer`, and `condition`
3. **Outlier Treatment** — Applied `Winsorizer` (quantile-based capping) on `mmr`, `odometer`, and `sellingprice`
4. **Encoding** — Label Encoding applied to all categorical features
5. **Scaling** — Standardized features using `StandardScaler`
6. **Model Training** — Linear Regression as baseline model
7. **Evaluation** — Mean Squared Error (MSE) and R² Score
8. **Cross-Validation** — 5-Fold Cross Validation for robust performance estimation
9. **Hyperparameter Tuning** — Ridge Regression optimized via `GridSearchCV` across multiple alpha values

---

## 🛠️ Tech Stack

`Python` · `Pandas` · `NumPy` · `Scikit-Learn` · `Seaborn` · `Matplotlib` · `feature-engine`

**Algorithms:** Linear Regression · Ridge Regression (GridSearchCV-tuned)

---

## 📁 Project Structure

```
selling-price-of-vehicles/
├── selling-price-of-vehicles.ipynb   # Full analysis & model notebook
└── README.md
```

---

## 🚀 Run This Project Locally

```bash
git clone https://github.com/vishnu-chaithanya-ds/selling-price-of-vehicles.git
cd selling-price-of-vehicles
pip install pandas numpy scikit-learn seaborn matplotlib feature-engine
jupyter notebook selling-price-of-vehicles.ipynb
```

---

## 👤 About Me

**Tadipatri Vishnu Chaithanya**
Aspiring Data Scientist | B.Tech — CSE (AI & ML)

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vishnuchaithanya.netlify.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tadipatri-vishnu-chaithanya-52817037b)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/vishnu-chaithanya-ds)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tadipatrivishnuchaithanya@gmail.com)

---

⭐ **If you found this project useful, consider giving it a star!**
