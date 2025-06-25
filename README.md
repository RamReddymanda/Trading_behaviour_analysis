# 📊 Trader Behavior Insights – Market Sentiment Analysis

This project explores how **market sentiment (Fear, Greed, etc.)** influences **trader behavior and performance** using real historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

## 🧠 Objective
- Understand the relationship between **trader profit/loss** and **market sentiment**
- Identify behavioral patterns based on **BUY/SELL decisions**
- Build a simple **machine learning model** to predict trade outcomes

## 📂 Datasets Used
1. **Hyperliquid Historical Trader Data**  
   - Fields: Account, Coin, Execution Price, Side, PnL, etc.

2. **Bitcoin Fear & Greed Index**  
   - Fields: Date, Sentiment Classification (Fear, Greed, etc.)

## 🔍 Key Insights
- **Highest Avg Profit:** During **Extreme Greed** when **selling**
- **Best Time to Buy:** During **Fear** or **Extreme Fear** (low prices, high upside)
- **Win Rate:** Majority of losses are rare (~8% of trades); market sentiment has predictive power
- **Best Performing Coin:** `HYPE` showed consistent profitability across all sentiments

## 📉 Sentiment-Based Strategy Summary

| Sentiment       | Best Action | Avg PnL (USD) | Win Rate |
|-----------------|-------------|---------------|----------|
| Fear            | BUY         | 209.65        | 26.3%    |
| Extreme Fear    | BUY         | 119.45        | 20.1%    |
| Greed           | SELL        | 111.02        | 46.9%    |
| Extreme Greed   | SELL        | 176.05        | 58.9%    |
| Neutral         | SELL        | 60.05         | 55.6%    |

> ✅ Buy when others panic.  
> ✅ Sell when others are greedy.

## Visualizations
Sentiment-wise profit/loss distribution

Coin-specific average PnL under different sentiments

BUY/SELL win rates across sentiments

## 🛠 Tech Stack
Python, Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn (ML Model)

Jupyter Notebook / Google Colab
## 🧪 ML Model Overview
- Built a **Random Forest Classifier** to predict trade outcome (Profit / No Profit)
- Input features: Coin, Side, Sentiment, Fee, Trade Size, etc.
- Sample prediction:

```plaintext
Trade 1: Not Profitable (Confidence: 100.00%)
Trade 2: Profitable (Confidence: 65.00%)
Trade 3: Not Profitable (Confidence: 89.00%)


