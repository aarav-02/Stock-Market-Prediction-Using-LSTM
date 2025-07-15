# 📈 Stock Price Forecasting using LSTM

A deep learning–based time‑series model to predict the next‑day closing price of stocks using historical financial data from Yahoo Finance. Built with Python and TensorFlow (Keras), this project demonstrates how LSTM networks can model temporal dependencies in financial data for price forecasting.

---

## 🔍 Project Overview

- **Objective** Predict next‑day stock closing prices using a 4‑layer LSTM neural network trained on 100‑day sliding windows.  
- **Problem Type** Time‑Series Forecasting / Regression  
- **Domain** Finance, Deep Learning, AI in Stock Market  

---

## 📊 Tech Stack

| Layer    | Tools & Libraries                               |
|----------|-------------------------------------------------|
| Language | **Python**                                      |
| DL / ML  | **TensorFlow / Keras**, **scikit‑learn**        |
| Data     | **yFinance**, **Pandas**, **NumPy**             |
| Viz      | **Matplotlib**, **Seaborn**                     |

---

## ⚙️ How It Works

1. **Data Collection**  
   Historical OHLCV data is fetched on the fly with `yfinance` for any valid ticker.

2. **Preprocessing**  
   - Focus on the **Close** price.  
   - Min‑max scaling.  
   - Build 100‑day rolling windows for LSTM input.

3. **Model Architecture**  
   - 4 stacked LSTM layers  
   - Dropout for regularization  
   - Dense output layer for regression

4. **Training**  
   80 % train / 20 % test split, optimized with Adam; early stopping to avoid overfitting.

5. **Evaluation**  
   Achieved **MAE < \$5** on unseen data across multiple tickers.

6. **Prediction**  
   Given the latest 100 days, the model outputs the forecasted next‑day closing price.

---

## 📈 Results

| Ticker | Test MAE | Test RMSE |
|--------|---------:|----------:|
| AAPL   | \$4.78   | \$6.12    |
| MSFT   | \$4.31   | \$5.79    |

Plots comparing actual vs. predicted prices are saved in the `plots/` directory.

---

## 📂 Folder Structure

LSTM-Stock-Prediction/

├── stock_predictor.ipynb # Main notebook

├── model/ # Saved weights 

├── plots/ # Output chart

├── README.md # Project doc (you’re reading it)

└── requirements.txt # Dependencies


---

## 📌 Key Features

- **Plug‑and‑Play** Specify any ticker symbol in one line.  
- **Modular Code** Clean functions for data prep, modeling, and evaluation.  
- **Visual Insights** Automatic generation of performance plots.  
- **Extensible** Ready for multi‑feature or multivariate inputs (e.g., technical indicators).

---

## 🧠 Future Work

- Add indicators (RSI, MACD, etc.).  
- Experiment with attention‑based seq‑to‑seq models.  
- Deploy as a Flask API or Streamlit app for live forecasts.

---

## ✅ Requirements

```bash
pip install -r requirements.txt

