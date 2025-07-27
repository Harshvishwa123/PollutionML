# 🌍 Pollution Control ML Analysis

A complete machine learning project for analyzing **air and water quality data** using multiple regression models. This project utilizes datasets from [Kaggle](https://www.kaggle.com/) to predict **Air Quality Index (AQI)** and analyze **Water Quality parameters**. The goal is to identify key pollutants affecting environmental health and evaluate model performance for effective pollution control measures.
## 🔗 Live Demo

🟢 Access the project overview here:  
👉 **[LIVE LINK](https://preview--hydroguard-ai.lovable.app/)**
👉 **[Earth Watch Pollution](https://earth-watch-pollution.lovable.app)**


---


## 📁 Datasets Used

### 1. **Air Quality Data**
- 📌 **Source**: Kaggle
- 🔢 **Shape**: 29,531 rows × 16 columns
- 🎯 **Target Variable**: `AQI (Air Quality Index)`
- 💡 **Key Features**: `PM2.5`, `PM10`, `NO`, `NO2`, `NOx`, `NH3`, `CO`, `SO2`, `O3`, `Benzene`, `Toluene`, `Xylene`

### 2. **Water Quality Data**
- 📌 **Source**: Kaggle
- 🔢 **Shape**: 1,991 rows × 12 columns
- 🎯 **Target Variable**: `STATION CODE` (Proxy for quality clustering)
- 💡 **Key Features**: `Temp`, `pH`, `D.O.`, `Conductivity`, `B.O.D.`, `Nitrates/Nitrites`, `Fecal Coliform`, `Total Coliform`, `Year`

---

## 🧽 Data Preprocessing

- ✅ Removed rows with missing target values
- ✅ Handled missing features with imputation/cleaning
- ✅ Applied `StandardScaler` for numerical feature scaling
- ✅ Encoded categorical variables (if needed)
- ✅ Split into 80% Train / 20% Test sets

---

## 🤖 Machine Learning Models Used

For both datasets, the following regression models were trained:
- `Random Forest Regressor`
- `Gradient Boosting Regressor`
- `Linear Regression`
- `Ridge Regression`
- `Lasso Regression`
- `Support Vector Regression (SVR)`

---

## 🔍 Air Quality Prediction Results

### ✅ Best Model: **Random Forest Regressor**
- 🧠 **Train R²**: 0.9842
- 🧪 **Test R²**: 0.8809
- 📉 **Test RMSE**: 36.71
- 🔁 **Cross-Validation Score**: 0.8865 ± 0.0087

### 📊 Feature Importance:
| Feature     | Importance |
|-------------|------------|
| PM2.5       | 0.5125     |
| PM10        | 0.1481     |
| CO          | 0.1247     |
| NO          | 0.0435     |
| Toluene     | 0.0420     |
| Others...   | <0.03      |

### 🧠 Model Performance Summary:

| Model                  | Test R² | RMSE     |
|------------------------|---------|----------|
| **Random Forest**      | 0.8809  | 36.71    |
| Gradient Boosting      | 0.8299  | 43.87    |
| Linear Regression      | 0.6636  | 61.70    |
| Ridge/Lasso Regression | 0.6636  | 61.70    |
| SVR                    | 0.6375  | 64.05    |

---

## 💧 Water Quality Prediction Results

### ✅ Best Model: **Random Forest Regressor**
- 🧠 **Train R²**: 0.9245
- 🧪 **Test R²**: 0.3895
- 📉 **Test RMSE**: 636.32
- 🔁 **Cross-Validation Score**: 0.4510 ± 0.0311

### 📊 Feature Importance:
| Feature                      | Importance |
|------------------------------|------------|
| Year                         | 0.2053     |
| Total Coliform               | 0.1507     |
| Conductivity                 | 0.1345     |
| Nitrates/Nitrites            | 0.1017     |
| Temperature                  | 0.1004     |
| Others...                    | <0.1       |

### 🧠 Model Performance Summary:

| Model                  | Test R² | RMSE     |
|------------------------|---------|----------|
| **Random Forest**      | 0.3895  | 636.32   |
| Gradient Boosting      | 0.3703  | 646.24   |
| Linear/Ridge/Lasso     | 0.15    | 749.06   |
| SVR                    | 0.0244  | 804.37   |

---

## 📌 Key Findings

### 🌫️ **Air Quality**
- `PM2.5`, `PM10`, and `CO` are the most significant pollutants.
- Random Forest performed the best with **Test R² of 0.88**.
- Linear models performed poorly due to complex feature interactions.

### 💧 **Water Quality**
- Model performance was weaker due to high variability in `STATION CODE`.
- Top features: `Year`, `Total Coliform`, and `Conductivity`.
- Need better target definition (e.g., water quality index) for improved modeling.

---

## 🛠️ Technologies Used
- Python 3.10+
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`
- Jupyter Notebook

