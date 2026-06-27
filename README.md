# Gold Price Prediction using Prophet

## 📌 Project Overview

This project demonstrates how to forecast **gold prices** using **Facebook Prophet**, a powerful time series forecasting library developed by Meta. The model is trained on historical gold price data and predicts future gold prices by automatically learning trends and seasonal patterns.

The project covers the complete workflow for time series forecasting, including data loading, preprocessing, visualization, model training, evaluation, and future prediction.

---

## 📊 Dataset

**Dataset:** Gold Price Data

The dataset contains historical gold price information with the following important columns:

- **Date** – Date of observation
- **GLD** – Gold price (target variable)

The dataset is downloaded directly from Kaggle using the `kagglehub` library.

---

## 🚀 Features

- Download dataset directly from Kaggle
- Data preprocessing for Prophet
- Time series visualization
- Train-test split (90% training, 10% testing)
- Gold price forecasting using Prophet
- Interactive forecast visualization
- Trend and seasonality analysis
- Model evaluation using RMSE
- Future gold price prediction
- Export future predictions to CSV

---

## 🛠 Technologies Used

- Python
- Pandas
- Prophet (Facebook Prophet)
- Plotly
- Matplotlib
- KaggleHub
- Statsmodels

---

## 📈 Workflow

### 1. Download Dataset

The dataset is downloaded automatically from Kaggle using KaggleHub.

### 2. Load the Dataset

Read the CSV file and inspect the data.

### 3. Data Preprocessing

Prophet requires the dataset to have two specific columns:

- **ds** → Date column
- **y** → Target value

The original columns are renamed as:

- `Date` → `ds`
- `GLD` → `y`

### 4. Data Visualization

Visualize historical gold prices to observe:

- Trend
- Seasonality
- Price fluctuations

### 5. Train-Test Split

The dataset is divided into:

- **90% Training Data**
- **10% Testing Data**

This allows the model to be evaluated on unseen data.

### 6. Train Prophet Model

A Prophet model is initialized and trained using the training dataset.

The model automatically learns:

- Overall trend
- Yearly seasonality
- Weekly seasonality
- Trend changes (changepoints)

### 7. Forecast Gold Prices

The trained model predicts gold prices for the testing period.

The forecast includes:

- **yhat** – Predicted gold price
- **yhat_lower** – Lower confidence interval
- **yhat_upper** – Upper confidence interval

### 8. Visualize Forecast

The project generates interactive visualizations showing:

- Historical prices
- Forecasted prices
- Confidence intervals

It also displays the forecast components:

- Trend
- Weekly seasonality
- Yearly seasonality

### 9. Evaluate the Model

The model's performance is evaluated using **Root Mean Squared Error (RMSE)**.

A lower RMSE indicates that the predicted values are closer to the actual values.

### 10. Future Forecasting

After evaluation, the model can be retrained using the complete dataset to forecast future gold prices for any desired time period, such as:

- Next 30 days
- Next 90 days
- Next 365 days

Future predictions can also be saved as a CSV file for further analysis.

---

## 📉 Evaluation Metric

The model uses **Root Mean Squared Error (RMSE)** to measure forecasting accuracy.

RMSE calculates the average difference between the predicted and actual gold prices. Lower RMSE values indicate better model performance.

---

## 📌 Future Improvements

- Hyperparameter tuning for Prophet
- Time series cross-validation
- Compare Prophet with ARIMA
- Compare Prophet with LSTM
- Incorporate external regressors (e.g., USD Index, Oil Prices)
- Deploy the model using Streamlit
- Build a real-time forecasting dashboard

---

## 🎯 Learning Outcomes

Through this project, you will learn:

- Time series forecasting concepts
- Data preprocessing for Prophet
- Forecast visualization techniques
- Trend and seasonality analysis
- Model evaluation using RMSE
- Future forecasting using historical data
