# Bitcoin High Price Prediction Using Machine Learning and Deep Learning

## 📌 Project Overview

This project focuses on predicting the **daily High Price of Bitcoin** using historical Bitcoin market data.

The project provides a comparative analysis of **statistical time-series models, machine learning models, and deep learning models**. In addition to price forecasting, the project explores **anomaly detection** and **Bitcoin return volatility modeling**.

The primary prediction target is the **Bitcoin High Price**.

---

## 🎯 Objectives

The main objectives of this project are:

* Explore historical Bitcoin price and trading-volume patterns.
* Analyze the statistical properties and stationarity of Bitcoin prices.
* Develop traditional time-series forecasting models.
* Develop machine learning models using historical and lag-based features.
* Develop an LSTM deep learning model for sequential price prediction.
* Compare the performance of different forecasting approaches.
* Detect unusual market observations using anomaly-detection techniques.
* Analyze Bitcoin return volatility using GARCH.

---

## 📊 Dataset

The project uses historical daily Bitcoin market data.

### Dataset Features

| Feature | Description                          |
| ------- | ------------------------------------ |
| Date    | Trading date                         |
| Open    | Opening Bitcoin price                |
| High    | Highest Bitcoin price during the day |
| Low     | Lowest Bitcoin price during the day  |
| Close   | Closing Bitcoin price                |
| Volume  | Daily trading volume                 |

### Dataset Information

* **Observations:** 5,296
* **Variables:** 6
* **Time period:** August 2010 – January 2025
* **Target variable:** Bitcoin `High` price

The original dataset contains price and volume values with currency symbols and separators, which are converted into numerical values during preprocessing.

---

## 🔧 Data Preprocessing

The following preprocessing steps are performed:

1. Convert price and volume columns from strings to numerical values.
2. Convert the `Date` column to datetime format.
3. Sort observations chronologically.
4. Set `Date` as the time-series index.
5. Check for missing values.
6. Preserve the OHLC and Volume variables for exploratory analysis and feature construction.

No missing values were identified in the original dataset.

---

## 📈 Exploratory Data Analysis

The project examines:

* Bitcoin price trends over time
* Daily trading volume
* Rolling mean
* Rolling standard deviation
* Price distributions
* Correlations between market variables
* Stationarity of the time series
* Log-transformed price behavior
* Bitcoin returns

The analysis highlights Bitcoin's long-term growth and periods of high market volatility.

---

## 📉 Stationarity Analysis

The Augmented Dickey-Fuller (ADF) test is used to examine whether the Bitcoin price series is stationary.

Because Bitcoin prices exhibit strong trends and changing variance, transformation techniques are explored to improve stationarity before applying statistical time-series modeling.

---

## 🤖 Models Used

### 1. ARIMA

The ARIMA model is used as a traditional statistical time-series forecasting approach.

Model:

```text
ARIMA(5,1,0)
```

---

### 2. XGBoost

XGBoost is used as a gradient-boosting machine learning model for Bitcoin High Price prediction.

---

### 3. LightGBM

LightGBM is another gradient-boosting model used to evaluate Bitcoin price prediction performance.

---

### 4. CatBoost

CatBoost is included as an additional boosting-based machine learning approach.

---

### 5. LSTM

A Long Short-Term Memory (LSTM) neural network is used to model sequential dependencies in Bitcoin prices.

The LSTM approach uses historical observations in a sliding-window structure to predict future values.

---

### 6. Isolation Forest

Isolation Forest is used for detecting unusual or anomalous market observations.

---

### 7. Hidden Markov Model (HMM)

A Gaussian Hidden Markov Model is used to identify different hidden market states and investigate unusual periods in Bitcoin price behavior.

---

### 8. GARCH

A GARCH model is used to analyze and forecast Bitcoin return volatility.

Model:

```text
GARCH(1,1)
```

This allows the project to investigate volatility clustering and persistent conditional volatility.

---

### 9. LSTM Autoencoder

An LSTM Autoencoder is additionally used for sequence-based anomaly detection.

---

## 📏 Evaluation Metrics

The forecasting models are evaluated using:

* **Mean Squared Error (MSE)**
* **R² Score**

Additional metrics such as Mean Absolute Error (MAE) are also used in the notebook where applicable.

### Metrics

**Mean Squared Error (MSE)** measures the average squared difference between actual and predicted values.

**R² Score** measures how well the model explains the variation in the target variable.

---

## 🛠️ Technologies and Libraries

### Programming Language

* Python

### Data Analysis

* NumPy
* Pandas

### Data Visualization

* Matplotlib
* Seaborn

### Statistical Modeling

* Statsmodels
* ARCH/GARCH

### Machine Learning

* Scikit-learn
* XGBoost
* LightGBM
* CatBoost

### Deep Learning

* TensorFlow / Keras
* LSTM

### Time-Series & Anomaly Detection

* ARIMA
* HMM
* Isolation Forest
* GARCH
* LSTM Autoencoder

---

## 📁 Project Structure

```text
Bitcoin-Price-Prediction/
│
├── Bitcoin_prediction.ipynb
│
├── data/
│   └── BTC-USD-Price-History-2010-2024.csv
│
├── results/
│   └── README.md
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Bitcoin-Price-Prediction.git
```

### 2. Navigate to the project directory

```bash
cd Bitcoin-Price-Prediction
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook Bitcoin_prediction.ipynb
```

Alternatively, the notebook can be opened directly using Google Colab.

---

## 📂 Dataset Path

The notebook should load the dataset using the relative path:

```python
df = pd.read_csv('data/BTC-USD-Price-History-2010-2024.csv')
```

This allows the notebook to work correctly when cloned from GitHub.

---

## 🔬 Project Workflow

```text
Historical Bitcoin Data
          ↓
Data Cleaning & Preprocessing
          ↓
Exploratory Data Analysis
          ↓
Stationarity Analysis
          ↓
Feature Engineering
          ↓
Model Development
          ↓
ARIMA / XGBoost / LightGBM / CatBoost
          ↓
LSTM Prediction
          ↓
Model Evaluation
          ↓
Anomaly Detection
          ↓
HMM / Isolation Forest / LSTM Autoencoder
          ↓
Volatility Analysis
          ↓
GARCH
```

---

## 📌 Key Focus

The main focus of this project is not only Bitcoin price prediction but also understanding different aspects of cryptocurrency market behavior through:

* Price forecasting
* Sequential modeling
* Statistical time-series analysis
* Machine learning
* Deep learning
* Anomaly detection
* Market-state analysis
* Volatility forecasting

---

## ⚠️ Disclaimer

This project is intended for **educational and research purposes only**.

Bitcoin prices are highly volatile and influenced by many external factors. Predictions generated by machine learning or statistical models should not be considered financial advice or guaranteed future prices.

---

## 👩‍💻 Author

**Priya Mali**

MSc Computer Science – Big Data Analytics

---

## ⭐ Acknowledgements

The project uses historical Bitcoin market data for academic and analytical purposes.

If you find this project useful, consider giving the repository a ⭐.
