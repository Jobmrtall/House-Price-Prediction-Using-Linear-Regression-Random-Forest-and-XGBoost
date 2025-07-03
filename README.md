
# 🏡 House Price Prediction using Regression and Ensemble Techniques

This project is built on the **[Kaggle House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)** dataset. It presents a complete machine learning pipeline to predict housing prices, from **missing value handling** and **feature engineering**, to **model training**, **PCA dimensionality reduction**, and **performance evaluation**.

---

## 🔧 Project Overview

This project showcases:
- Thoughtful **missing value imputation** using **KNN imputation** guided by **Spearman correlation**.
- Strategic **log transformation**, creation of meaningful new features, and **one-hot encoding**.
- Implementation and tuning of multiple models including **regularized regression** and **ensemble techniques**.
- Comparison of model performance with and without **Principal Component Analysis (PCA)**.

---

## 🧹 Data Preprocessing and Feature Engineering

### ✅ Missing Value Handling
- Applied **KNN imputation** for features with moderate-to-strong Spearman correlations (ρ > 0.2).
- Used **mean imputation** for low-correlation or sparse features like `BsmtFinSF2`, `BsmtHalfBath`, etc.

### 🧠 Feature Engineering
- Created new informative variables:
  - `HouseAge = YrSold - YearBuilt`
  - `RemodAge = YrSold - YearRemodAdd`
  - `GarageAge = YrSold - GarageYrBlt`
  - `RemodDelay = YearRemodAdd - YearBuilt`
- Applied **log transformation** to skewed numeric features for improved model fit.
- Encoded categorical features using **one-hot encoding**.

---

## 🔬 Dimensionality Reduction

- Applied **PCA** (Principal Component Analysis) after standardization.
- Compared model performance with and without PCA to assess the tradeoff between dimensionality and accuracy.

---

## 🤖 Models Developed

- **Linear Regression**
- **Lasso Regression**
- **Ridge Regression**
- **ElasticNet**
- **Random Forest**
- **XGBoost**

Models were trained using **pipelines**, hyperparameter-tuned using **GridSearchCV** or **RandomizedSearchCV**, and evaluated via **cross-validation** and test metrics.

---

## 📊 Evaluation Metrics

Performance was measured using:
- **Cross-validated R² (CV R²)**
- **Test R²**
- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

### ✅ Final Results

Among all models, **ElasticNet** achieved the best test performance in terms of **R², MSE, MAE, and RMSE**, outperforming Random Forest and XGBoost. PCA-based models slightly underperformed, showing that dimensionality reduction wasn't necessary due to effective feature selection.

---

## 📁 Project Structure

```
├── data/                     # Dataset (downloaded from Kaggle)
├── notebook/                 # Jupyter Notebook with full pipeline
├── results/                  # Performance metrics and plots
├── README.md                 # Project summary
```

---

## 🔗 View Full Project

📎 [GitHub Repository Link]([https://github.com/yourusername/your-repo](https://github.com/Jobmrtall/House-Price-Prediction-Using-Linear-Regression-Random-Forest-and-XGBoost/blob/main/House_Price_Prediction_Using_Linear_Regression_%2CRandom_Forest_and_XGBoost.ipynb))

---

## 🚀 Tools & Libraries Used

- Python, Pandas, NumPy, Seaborn, Matplotlib
- Scikit-learn, XGBoost
- PCA, Regularization, Hyperparameter Tuning
