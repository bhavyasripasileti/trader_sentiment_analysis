# 📊 Trader Performance vs Market Sentiment (Fear & Greed)

## 📌 Objective
The goal of this project is to analyze how **Bitcoin market sentiment (Fear vs Greed)**
influences **trader behavior and performance** on the Hyperliquid platform, and to derive
**actionable trading insights** that can inform better trading strategies.

---

## 📂 Datasets Used

### 1. Bitcoin Fear & Greed Index
- **File:** `fear_greed_index.csv`
- **Key columns:**
  - `date` – Daily date  
  - `value` – Fear & Greed index value  
  - `classification` – Fear / Greed  

### 2. Hyperliquid Historical Trader Data
- **File:** `historical_data.csv`
- **Key columns:**
  - `Account` – Trader identifier  
  - `Side` – Buy / Sell  
  - `Closed PnL` – Profit or Loss per trade  
  - `Size USD` – Trade size  
  - `Timestamp IST` – Trade execution time  

---

## 🧪 Methodology

### Data Loading & Inspection
- Loaded both datasets and inspected schema, size, and data quality.
- Identified correct timestamp and sentiment columns.

### Data Cleaning & Preparation
- Converted timestamps to datetime format (`dayfirst=True`).
- Aligned both datasets at **daily granularity**.
- Renamed columns for consistency and clarity.

### Feature Engineering
- Daily PnL per trader  
- Win rate  
- Trade frequency  
- Average trade size  
- Long/short (buy) ratio  

### Sentiment-Based Analysis
- Compared trader performance on **Fear vs Greed** days.
- Analyzed behavioral changes such as trade frequency and position bias.

### Trader Segmentation
- Frequent vs Infrequent traders  
- Consistent vs Inconsistent traders (based on win rate)

---

## 📈 Key Insights
- Trader PnL shows **higher volatility during Fear periods** compared to Greed periods.
- Trade frequency increases during Greed days, but **win rate does not improve proportionally**, indicating potential overtrading.
- Consistent traders maintain relatively stable behavior across sentiment regimes, suggesting strong risk management.

---

## 🎯 Actionable Strategy Recommendations
- Reduce exposure during Fear periods to limit drawdowns and volatility.
- Increase trade activity during Greed periods only for consistent traders with historically higher win rates.
- Avoid aggressive scaling of trade frequency without evidence of improved performance.

---

## ▶️ How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/bhavyasripasileti/trader_sentiment_analysis.git

2. Navigate to the project folder:
   ```bash
   cd trader_sentiment_analysis


3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn


4. Start Jupyter Notebook:
   ```bash
   python -m notebook

  Open analysis.ipynb and run all cells.

## 📁Project Structure

trader_sentiment_analysis/
│
├── analysis.ipynb
├── README.md
└── data/

    ├── fear_greed_index.csv
    └── historical_data.csv


## 👤 Author

Bhavya Sri Pasileti

📧 bhavyasripasileti@gmail.com
