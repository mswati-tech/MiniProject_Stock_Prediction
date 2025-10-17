# Stock Price and Trend Prediction with LSTM & CNN Models

This repository provides an end-to-end pipeline for **stock price regression** and **trend classification** using deep learning techniques (LSTM, CNN, and hybrid CNN-LSTM). The project allows predicting next-day stock prices and trends (up/down) from historical stock market data.

---

## Datasets

Link: https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data

---

## Features

* **Data Preprocessing & Feature Engineering**

  * Computes SMA, Bollinger Bands, RSI, MACD
  * Normalizes features using MinMaxScaler
* **Sequence Generation**

  * Converts time-series stock data into supervised sequences for regression and classification
* **Models**

  * CNN-LSTM hybrid model for regression
  * Standalone LSTM and CNN models for regression
  * LSTM-based classifier for trend prediction
* **Evaluation Metrics**

  * Regression: RMSE, MAE, R²
  * Classification: Accuracy, F1 Score
* **Visualizations**

  * Actual vs predicted stock prices
  * Actual vs predicted trends
* **Memory Optimized**

  * Efficient use of TensorFlow/Keras sessions and garbage collection

---

## Usage

1. Prepare CSV files for each stock with the following columns atleast from 3-January-2000 to 4-January-2005 (five years):

   Date, Open, High, Low, Close, Volume


2. Update the `ticker_to_file` mapping if needed.

3. Run the main script:

python miniproject2_code.py

4. Input the stock ticker and prediction type (e.g., `NEXT DAY`) when prompted.

---

## Project Structure

├── miniproject2_code.py               # Main script with training, evaluation, and visualization

├── data/                 # Folder containing CSV stock data

├── models/               # Saved models

├── utils.py              # Helper functions for preprocessing, sequences, and memory cleanup

├── README.md

## Models

| Model Type      | Purpose                        |
| --------------- | ------------------------------ |
| CNN-LSTM        | Regression (Price Prediction)  |
| LSTM            | Regression (Price Prediction)  |
| CNN             | Regression (Price Prediction)  |
| LSTM Classifier | Classification (Trend Up/Down) |

---

## Evaluation

* **Regression Metrics**: RMSE, MAE, R²
* **Classification Metrics**: Accuracy, F1 Score

Example output:

```
CNN-LSTM evaluation:
RMSE: 12.3456 | MAE: 8.5678 | R2: 0.89
Trend classification evaluation:
Accuracy: 0.78 | F1 Score: 0.81
```

---

## Visualization

* **Price Prediction Plot**: Shows actual vs predicted stock prices
* **Trend Prediction Plot**: Shows predicted vs actual trends (up/down)
* **Interactive Parameters**:

  * Window size for trend visualization
  * Probability threshold for trend classification

---

## Outputs

---

Added a **screenshot of the outputs** in the README for better clarity.

---
