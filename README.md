# Hourly Crypto Momentum Strategy


## Current Status & Next Steps

This project is **in active development**. 

---

This project builds and tests an **algorithmic trading strategy** for the **cryptocurrency market**.  
The focus is on understanding whether technical, sentiment, and fundamental indicators contain **predictive power** for short-term market direction.

---

## Data
- **Source:** Top 100 market-cap cryptocurrencies available on Binance.  
- **Frequency:** Hourly candles (open, high, low, close, volume).  
- Additional data includes **Sentiment, market cap, age, and other coin-level features**.

---

## Project Structure

### **A. Technical Indicator Analysis**
- `A_MAD_indicator.ipynb` — Tests **Moving Average Distance (MAD)** for predictive power using regression methods inspired by *Avramov, Kaplanski & Subrahmanyam (2018)*.  
- `B_RSI_indicator.ipynb` — Evaluates the **Relative Strength Index (RSI)** and its ability to predict future returns, comparing standard and modified RSI configurations.  
- `C_Volume_indicators.ipynb` — Analyzes **volume-based metrics** such as volume spikes, volume/price divergence, and volume-weighted momentum.

### **B. Sentiment and Fundamentals**
- `D_Sentiment_indicator.ipynb` — Incorporates **sentiment data** (social media, aggregated market mood) to assess its predictive relationship with price movements.  
- `E_fundamentals_indicators.ipynb` — Examines **fundamental attributes** (market cap, age, supply metrics) and their influence on volatility and trend strength.

### **C. Regime Labeling and Prediction**
- `F_Regime_Labels.ipynb` — Defines **market regimes** based on price trends:  
  - **1 → Uptrend**  
  - **-1 → Downtrend**  
  - **0 → Choppy / sideways market**  
- `G_Regime_Prediction.ipynb` — Builds a **predictive model** to forecast the regime **10 hours ahead** using the most significant features discovered in earlier notebooks.

### **D. Final Strategy**
- `H_Final_Strategy.ipynb` — Combines all modules into a **trading system**:  
  - Converts model predictions into **confidence-weighted trade signals**.  
  - Applies **dynamic stop-loss and take-profit** levels based on each coin’s volatility.  
  - Evaluates strategy performance across assets and regimes.

---

## Methodology Summary
1. **Feature discovery:** Identify indicators with significant predictive power.  
2. **Labeling:** Define the market state (up, down, choppy).  
3. **Modeling:** Train a model to predict the regime 10 hours forward.  
4. **Signal generation:** Use model confidence to determine trade entries.  
5. **Risk management:** Adaptive stop-loss / take-profit based on volatility.

---

## Goal
To build an interpretable, data-driven trading framework that links:
- **Technical indicators** (momentum, trend, volatility)
- **Sentiment and fundamental data**
- **Machine learning predictions**
  
into one unified strategy for the cryptocurrency market.

---

**And that’s it — good luck to us! **
