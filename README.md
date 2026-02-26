# Trader Performance vs Market Sentiment Analysis

##  Project Overview
This project analyzes how Bitcoin market sentiment (Fear/Greed Index) influences trader behavior and performance on Hyperliquid.  
The goal is to uncover behavioral patterns that can inform smarter trading strategies.

---

## Datasets

### 1. Bitcoin Market Sentiment
- Date
- Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

### 2. Hyperliquid Historical Trader Data
- Account
- Execution Price
- Trade Size (USD & Tokens)
- Side (Buy/Sell)
- Timestamp
- Closed PnL
- Fees
- Trade metadata

---

##  Methodology

### Data Preparation
- Checked missing values and duplicates
- Converted timestamps to daily level
- Aligned sentiment and trading data by date
- Merged datasets

### Feature Engineering
- Daily PnL per account
- Win rate (PnL > 0)
- Trade frequency per account
- Average trade size
- Trades per day
- Trader segmentation:
  - High vs Low frequency
  - Consistent vs Inconsistent performers

---

##  Key Findings

### 1️⃣ Performance vs Sentiment
- **Extreme Greed days show the highest average PnL**
- Extreme Fear days show weakest performance

### 2️⃣ Behavioral Shifts
- Trade frequency increases during Greed periods
- Fear periods show reduced activity but larger individual trades

### 3️⃣ Trader Segmentation Insights
- High-frequency traders outperform during Greed
- Low-frequency traders perform relatively better during Fear
- Inconsistent traders show higher variance returns

---

##  Strategy Recommendations

1. **Increase controlled trade frequency during Extreme Greed**
   - Momentum conditions favor active traders.

2. **Reduce leverage and exposure during Extreme Fear**
   - Focus on selective trades only for consistent performers.

---

##  Key Visualizations

- Average PnL by Sentiment
- Win Rate by Sentiment
- Segment vs Sentiment Heatmap

(See `/images` folder for exported charts)

---

## ▶️ How to Run

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
