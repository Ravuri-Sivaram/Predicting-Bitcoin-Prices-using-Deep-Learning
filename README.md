# Predicting-Bitcoin-Prices-using-Deep-Learning
With the rise of the crypto digital era, more heads have turned towards the digital market for investments. This gives us the opportunity to create a model capable of predicting cryptocurrencies — primarily Bitcoin. With vast amounts of data being generated and recorded daily, we are approaching an era where such predictions can be accurate. This undergraduate project demonstrates how a well-trained machine learning model, when given the right data and computing power, can effectively forecast the price of a cryptocurrency.

This project uses a Long Short-Term Memory (LSTM) Recurrent Neural Network to predict the closing price of Bitcoin. The model is trained on historical data and visualizes the actual vs. predicted prices with strong performance metrics.

## 📊 Dataset

- Source: [Yahoo Finance](https://finance.yahoo.com/quote/BTC-USD/)
- File used: `BTC-USD_1.csv`
- Features: `Open`, `High`, `Low`, `Close`, `Volume`
- Date Range: Includes data before and after January 1, 2020 (split into training and testing)

## 🧠 Model Overview

- Type: LSTM (Recurrent Neural Network)
- Sequence Length: 60 days
- Layers:
  - LSTM layer with 50 units
  - Dropout layer (0.2)
  - Dense output layer
- Optimizer: `adam`
- Loss: `mean_squared_error`

## ⚙️ Workflow

1. Load and preprocess data using `MinMaxScaler`
2. Create time series sequences (60-day windows)
3. Train LSTM model on data before 2020
4. Predict Bitcoin prices on data after 2020
5. Visualize training/validation loss and price predictions
6. Evaluate with MAE, MSE, RMSE, and R² Score

## 📈 Results

| Metric     | Value        |
|------------|--------------|
| MAE        | 2892.07      |
| MSE        | 31,747,013.27|
| RMSE       | 5634.45      |
| R² Score   | 0.9012       |

The model successfully captures the trend of Bitcoin prices with an R² of 90%.

## 📉 Visualization

- Training vs. Validation Loss  
- Actual vs. Predicted Bitcoin Prices

## 📦 Requirements

To run the code, install the following dependencies:

```bash
pip install -r requirements.txt
