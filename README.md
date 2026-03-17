# Gold Price Trend Prediction 📈

**Group Members:** Nazneen Khanmongkhol, Jinnaphat Guntawang, Sopon Pleangnoi  
**Academic Context:** EGCI 463: Pattern Recognition | Final Project  
**Institution:** Mahidol University International College  

## 📌 Project Overview
This repository contains our final project for Pattern Recognition. We wanted to see if we could predict daily gold price movements using various machine learning models. Since the stock market is incredibly noisy and volatile, this was mostly an experimental dive to compare how traditional ML stacks up against deep learning.

## 📊 Dataset & Features
We used daily financial observations from 2015 to 2025. 
* **Target:** Gold Close Price
* **Indicators:** Crude Oil, USD Index, DJI, Copper, NASDAQ, S&P 500, and Bitcoin (BTC)
* **Added Features:** We engineered a few extra data points to help the models, including lag features, moving averages (5, 20, and 50-day), and basic volatility metrics.

## 🛠️ Models We Tried
We classified daily movements into Down (0), Up (1), or Neutral (2) using a custom trend-labeling function, and tested three approaches:
1. **Random Forest:** Our traditional machine learning baseline.
2. **LSTM Regression:** A sequential deep learning model to try and catch time-based patterns.
3. **Autoencoder + MLP:** An experimental feature-extraction approach.

## 🚀 What We Found
Predicting financial markets is definitely tricky! 
* **Random Forest** ended up being our most stable and reliable model, hitting about 58% accuracy. It turns out our engineered features (like moving averages) were way more helpful to the model than the raw financial indices.
* **Autoencoder & LSTM** struggled a lot more with the market noise. They had a hard time predicting actual shifts and tended to just play it safe by guessing "Neutral" most of the time.

## 💻 How to Run (Disclaimer)
*Note: This is an archived class project. Some of the original local CSV files may be missing from the `/data` folder, and the notebook might require some tweaks to run perfectly out of the box today.*

1. Clone this repository.
2. Ensure you have the necessary datasets in a `/data` folder.
3. Install dependencies: `pip install pandas numpy scikit-learn tensorflow matplotlib seaborn`
4. Open and run the Colab notebook.
