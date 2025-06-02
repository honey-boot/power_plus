 ⚡ PowerPulse: Household Energy Consumption Prediction

A machine learning project to predict household electricity usage using regression models. This project involves data preprocessing, exploratory data analysis (EDA), model building, hyperparameter tuning, and evaluation based on performance metrics.

---

## 📂 Dataset

- **Name**: Individual Household Electric Power Consumption
- **Source**: UCI Machine Learning Repository
- **Duration**: 4 years of data
- **Target Variable**: `Global_active_power` (kilowatts)

---

## 📌 Project Workflow

### 1️⃣ Data Preprocessing
- Handled missing values
- Converted data types (to `float`)
- Transformed `Date` and `Time` into a single `Datetime` column
- Extracted time-based features:
  - Hour
  - Day
  - Month
  - Weekday
  - Is weekend

### 2️⃣ Exploratory Data Analysis (EDA)
- Distribution plot of `Global_active_power`
- Daily average consumption trends
- Correlation heatmap of numeric and time-based features

### 3️⃣ Feature Engineering
- Dropped irrelevant columns (original datetime)
- Prepared input (`X`) and target (`y`)
- Train-test split (80% train, 20% test)

### 4️⃣ Model Building
- **Linear Regression** (baseline model)
- **Random Forest Regressor** (with hyperparameter tuning using `RandomizedSearchCV`)
- **Gradient Boosting Regressor** (with tuning)

### 5️⃣ Evaluation Metrics
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

### 6️⃣ Visualizations
- Actual vs Predicted plots for each model
- Feature Importance for Random Forest & Gradient Boosting
- Coefficients plot for Linear Regression

---

## 📊 Best Model Performance

| Model               | MAE       | RMSE      | R² Score   |
|--------------------|-----------|-----------|------------|
| Linear Regression  | 0.0257    | 0.0402    | 0.9986     |
| Random Forest       | 0.0201    | 0.0343    | 0.9990     |
| Gradient Boosting   | **0.0183**| **0.0304**| **0.9992** |

✅ **Gradient Boosting** gave the best performance among all models.

---

## 📎 Requirements

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

Install dependencies:
```bash
pip install -r requirements.txt
