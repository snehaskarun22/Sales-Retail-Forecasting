# 📈 Retail Sales Forecasting

A machine learning project for forecasting **retail product sales** using historical store, product, pricing, promotion, weather, and seasonal information.

The project applies feature engineering and compares multiple regression models, including **Polynomial Regression, Random Forest, and LightGBM**, to predict the number of units sold.

---

## 🎯 Project Objective

Accurate sales forecasting can help retailers improve:

- Inventory planning
- Stock management
- Demand estimation
- Procurement decisions
- Sales planning

The objective of this project is to build a machine learning model that can predict **Units Sold** using historical retail data and generate future sales forecasts.

---

## 📊 Dataset

The project uses a retail inventory forecasting dataset containing information related to:

- Date
- Store ID
- Product ID
- Category
- Region
- Inventory Level
- Units Sold
- Units Ordered
- Demand Forecast
- Price
- Discount
- Weather Condition
- Holiday/Promotion
- Competitor Pricing
- Seasonality

The target variable is:

```text
Units Sold
```

---

## 🔍 Feature Engineering

The date column was converted into useful time-based features:

```text
Year
Month
DayOfWeek
```

The data was also sorted by store, product, and date.

To capture historical sales patterns, lag features were created:

```text
Units Sold_lag1
Units Sold_lag2
Units Sold_lag3
```

These features represent previous sales values for the same store-product combination. :contentReference[oaicite:2]{index=2}

---

## 🧠 Machine Learning Models

The project compares different regression algorithms:

### 1. Polynomial Regression

Used as a baseline model to capture nonlinear relationships.

### 2. Random Forest Regressor

An ensemble tree-based model used to capture nonlinear feature interactions.

### 3. LightGBM Regressor

A gradient boosting model selected as the final forecasting model because of its strong predictive performance.

The LightGBM configuration includes:

```text
num_leaves = 31
learning_rate = 0.05
n_estimators = 300
```

---

## 🔄 Machine Learning Pipeline

```text
Raw Retail Dataset
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Date Feature Engineering
        ↓
Lag Feature Creation
        ↓
Categorical Feature Handling
        ↓
Train / Test Split
        ↓
Model Training
        ↓
Model Comparison
        ↓
LightGBM Selection
        ↓
Future Sales Forecast
```

---

## 📈 Model Performance

The LightGBM model achieved the following performance on the test set:

| Metric | Score |
|---|---:|
| MAE | 7.23 |
| RMSE | 8.47 |
| R² | 0.994 |

The model was trained using 36,500 rows and evaluated on 36,600 testing rows. :contentReference[oaicite:3]{index=3} :contentReference[oaicite:4]{index=4}

### Metric Interpretation

**MAE (Mean Absolute Error)**

Measures the average absolute difference between actual and predicted sales.

**RMSE (Root Mean Squared Error)**

Penalizes larger prediction errors more strongly.

**R² (R-squared)**

Measures how much of the variation in the target variable is explained by the model.

---

## 🔮 Future Sales Forecasting

After training, the LightGBM model is used to predict future sales.

The project generates:

- Date
- Store ID
- Product ID
- Predicted Units Sold

A **30-day future sales forecast** is also visualized by aggregating predicted units sold by date. :contentReference[oaicite:5]{index=5}

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming |
| Pandas | Data manipulation |
| NumPy | Numerical computation |
| Scikit-learn | Machine learning and evaluation |
| LightGBM | Gradient boosting forecasting |
| Matplotlib | Visualization |
| Seaborn | Data visualization |
| Google Colab | Development environment |

---



## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

```text
pandas
numpy
scikit-learn
lightgbm
matplotlib
seaborn
```

---

## 🚀 How to Run

Open the notebook:

```text
Retail_Sales_Forecasting.ipynb
```

Run the notebook cells in order.

The notebook performs:

1. Data loading
2. Data preprocessing
3. Exploratory data analysis
4. Feature engineering
5. Lag feature creation
6. Model training
7. Model evaluation
8. Model comparison
9. Future sales forecasting
10. Forecast visualization

---

## 📊 Results

The final LightGBM model provides highly accurate predictions on the test data, with an R² of approximately **0.994**.

The model is then used to generate future sales predictions for store-product combinations.

---

## 🔮 Future Improvements

- Incorporate more advanced time-series models
- Add automated hyperparameter tuning
- Develop an interactive sales forecasting dashboard
- Add external economic and market indicators
- Implement real-time forecasting
- Deploy the model as a web application
- Add uncertainty intervals to future predictions

---

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Exploratory Data Analysis
- Feature Engineering
- Time-based Feature Engineering
- Lag Feature Creation
- Regression Modeling
- Model Comparison
- LightGBM
- Model Evaluation
- Sales Forecasting
- Data Visualization

---

## 👩‍💻 Author

**Sneha S Karun**

MS AI & Data Science

GitHub: `https://github.com/snehaskarun22`

LinkedIn: `https://www.linkedin.com/in/sneha-s-karun-ba8397330/`

---


