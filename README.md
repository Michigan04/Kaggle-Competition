# Taxi Fare Prediction - Machine Learning Pipeline

## 📌 Project Overview

This project builds a **machine learning regression pipeline** to predict **taxi trip total amount** using trip-related features.
The dataset is provided as part of a **Kaggle assignment** and includes trip details such as:

* Trip distance
* Passenger count
* Pickup & Dropoff time
* Payment type
* Location IDs
* Additional charges

The goal is to **predict `total_amount`** using multiple regression models and select the best performing one.

---

## 📂 Dataset

The dataset contains:

### Training Dataset

* **Rows:** 10,000
* **Columns:** 17
* **Target Variable:** `total_amount`

### Test Dataset

* **Rows:** 1,500
* **Columns:** 17

---

## ⚙️ Libraries Used

```python
scikit-learn
pandas
numpy
matplotlib
seaborn
```

Models used:

* Linear Regression
* Ridge Regression
* Lasso Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor
* Support Vector Regressor (SVR)

---

## 🔍 Exploratory Data Analysis

### 1. Data Inspection

* Checked data types
* Verified missing values
* Checked duplicates

### 2. Missing Values

Handled using:

* **Numerical Features** → Mean Imputation
* **Categorical Features** → Most Frequent (Mode)

---

## 📊 Data Visualization

Visualizations created:

* Distribution of `total_amount`
* Scatter plot: `trip_distance vs total_amount`
* Payment type frequency
* Outlier detection using boxplots

### Key Insight

* Most trips fall within **lower fare range**
* Short-distance trips dominate dataset

---

## 🧹 Feature Engineering

### Datetime Processing

Created new features:

* `pickup_hour`
* `trip_duration`

Removed:

* `tpep_pickup_datetime`
* `tpep_dropoff_datetime`

---

## 🔄 Preprocessing Pipeline

### Numerical Features

* Mean Imputation
* Standard Scaling

### Categorical Features

* Mode Imputation
* One Hot Encoding

Used:

* `Pipeline`
* `ColumnTransformer`

---

## 🤖 Model Training

Multiple models trained and evaluated:

| Model          | R2 Score |
| -------------- | -------- |
| Decision Tree  | 0.9296   |
| Gradient Boost | 0.9126   |
| Random Forest  | 0.8978   |
| Ridge          | 0.8546   |
| Linear         | 0.8543   |
| Lasso          | 0.8216   |
| SVR            | 0.6250   |

---

## 🔧 Hyperparameter Tuning

### Random Forest

Best Parameters:

```
max_depth = 15
n_estimators = 200
```

### Decision Tree

Best Parameters:

```
max_depth = 10
min_samples_split = 10
```

### Gradient Boosting

Best Parameters:

```
learning_rate = 0.05
max_depth = 5
n_estimators = 200
```

---

## 🏆 Final Model

Final model selected:

**Gradient Boosting Regressor**

Reasons:

* High performance
* Robust to outliers
* Good generalization

---

## 🚀 Final Pipeline

Steps:

1. Data preprocessing
2. Feature scaling
3. One-hot encoding
4. Gradient Boosting Regressor

---

## 📤 Submission

Predictions generated for test dataset:

```python
submission.csv
```

Format:

| id | total_amount |
| -- | ------------ |

---

## 📈 Project Workflow

```
Load Data
   ↓
EDA
   ↓
Feature Engineering
   ↓
Preprocessing Pipeline
   ↓
Model Training
   ↓
Hyperparameter Tuning
   ↓
Model Comparison
   ↓
Final Model
   ↓
Prediction
   ↓
Submission File
```

---

## 📌 Key Highlights

✅ End-to-End ML Pipeline
✅ Multiple Model Comparison
✅ Hyperparameter Tuning
✅ Feature Engineering
✅ Production-Ready Pipeline

---

## 🧠 Future Improvements

* Try XGBoost / LightGBM
* Feature importance analysis
* Cross validation improvement
* Ensemble methods

---

## 👨‍💻 Author

Machine Learning Assignment - Taxi Fare Prediction

---

## 📁 Output

```
submission.csv
```

Ready for Kaggle submission 🚀

