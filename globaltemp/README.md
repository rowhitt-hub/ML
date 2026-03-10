

Global Temperature Forecasting using Time Series Models

This project analyzes historical global temperature data and builds forecasting models to predict future temperatures using classical **time series techniques**.

The goal of the project is to explore how statistical forecasting models such as **SARIMA** and **Holt-Winters Exponential Smoothing** can be used to model long-term temperature trends.

 
 Project Overview

Climate data often exhibits:

* Long-term trends
* Seasonality
* Temporal dependencies

In this project, we:

1. Perform **Exploratory Data Analysis (EDA)**
2. Check **time series stationarity**
3. Apply **differencing** when necessary
4. Train two forecasting models
5. Compare model performance
6. Generate **future temperature forecasts**

---

# 🗂 Dataset

Dataset used: **Global Land Temperatures**

Typical columns used in this project:

* `dt` → Date
* `LandAverageTemperature` → Global average land temperature

Steps applied:

* Converted date column to datetime
* Set date as index
* Removed missing values

---

# ⚙️ Project Workflow

## 1️⃣ Data Loading & Cleaning

* Load dataset using Pandas
* Convert date column to datetime
* Set date as index
* Select temperature column
* Remove missing values

---

## 2️⃣ Exploratory Data Analysis

We visualize the historical temperature trend to observe:

* long term warming trend
* seasonal fluctuations

Visualization includes:

* Time series temperature plot
* Seasonal decomposition

---

## 3️⃣ Seasonal Decomposition

The series is decomposed into:

* **Trend**
* **Seasonality**
* **Residual noise**

This helps understand the structure of the data before modeling.

---

## 4️⃣ Stationarity Check

Stationarity is tested using the **Augmented Dickey-Fuller (ADF) Test**.

If the series is non-stationary:

* First order **differencing** is applied

This step is necessary for models like SARIMA.

---

## 5️⃣ Train-Test Split

The dataset is split into:

* **80% training data**
* **20% testing data**

This allows us to evaluate forecasting performance.

---

# 🤖 Models Implemented

## 1️⃣ SARIMA (Seasonal ARIMA)

SARIMA models both:

* **Autoregressive components**
* **Moving averages**
* **Seasonal patterns**

Model parameters used:

```
SARIMA (1,1,1) (1,1,1,12)
```

This allows the model to capture **yearly seasonal effects**.

---

## 2️⃣ Holt-Winters Exponential Smoothing

Holt-Winters is effective for:

* Data with **trend**
* **Seasonality**

The additive seasonal model was used with:

```
seasonal_periods = 12
```

---

# 📈 Forecast Visualization

The forecasts are plotted alongside:

* Training data
* Test data
* Model predictions

This helps visually compare the model performance.

---

# 📏 Model Evaluation

Models are evaluated using **Root Mean Squared Error (RMSE)**.

```
RMSE = sqrt(mean_squared_error)
```

Lower RMSE indicates a better forecasting model.

Example output:

| Model        | RMSE |
| ------------ | ---- |
| SARIMA       | X.XX |
| Holt-Winters | X.XX |

---

# 🔮 Future Forecasting

The final SARIMA model is used to forecast **future temperatures for 120 months** (~10 years).

The forecast plot includes:

* Historical temperature data
* Predicted future temperature trend

---

# 🧰 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn

---

# 📁 Project Structure

```
temperature-forecasting/
│
├── temperature forecasting.ipynb
├── GlobalTemperatures.csv
└── README.md
```

---

# 🚀 How to Run the Project

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/temperature-forecasting.git
```

---

### 2️⃣ Install dependencies

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
```

---

### 3️⃣ Run the notebook

Open and run:

```
temperature forecasting.ipynb
```

---

# 📌 Key Learnings

This project demonstrates:

* Time series preprocessing
* Stationarity testing
* Seasonal decomposition
* SARIMA modeling
* Holt-Winters forecasting
* Model comparison using RMSE

It serves as a **good beginner project for learning time series forecasting.**

---

# 📬 Future Improvements

Possible extensions:

* Hyperparameter tuning for SARIMA
* AutoARIMA model selection
* Prophet forecasting model
* LSTM deep learning forecasting
* Climate anomaly detection

---

