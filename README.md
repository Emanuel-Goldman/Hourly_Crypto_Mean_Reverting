# 🪙 Hourly Crypto Momentum Strategy

This project builds and tests an **algorithmic trading strategy** for the **cryptocurrency market** using **hourly candles** from Binance.  
The focus is on understanding whether technical, sentiment, and fundamental indicators contain **predictive power** for short-term market direction.

---

## 📊 Data
- **Source:** Top 100 market-cap cryptocurrencies available on Binance.  
- **Frequency:** Hourly candles (open, high, low, close, volume).  
- Additional data includes **market cap, age, and other coin-level features**.

---

## 🧠 Project Structure

### **A. Technical Indicator Analysis**
- `A_MAD_indicator.ipynb`: Tests **Moving Average Distance (MAD)** for predictive power, following *Avramov, Kaplanski & Subrahmanyam (2018)*.
- `B_RSI_indicator.ipynb`: Tests **Relative Strength Index (RSI)** and its variants as predictors of future returns.
- `C_Volume_RSI.ipynb`: Extends analysis using **volume-adjusted RSI** and other momentum indicators.

### **B. Regime Definition and Prediction**
- `D_Regime_Labels.ipynb`: Defines market regimes based on price behavior.  
  - **1** → Uptrend  
  - **-1** → Downtrend  
  - **0** → Choppy / sideways market  
- `E_Regime_Prediction.ipynb`: Builds models to **predict the regime 10 hours ahead** using selected features.

### **C. Strategy Construction**
- `F_Final_Strategy.ipynb`:  
  - Converts model predictions into **trading signals** based on prediction confidence.  
  - Executes trades with **dynamic stop-loss and take-profit** levels calibrated to each coin’s volatility.

---

## ⚙️ Methodology Summary
1. **Feature discovery:** Identify indicators with significant predictive power.  
2. **Labeling:** Define the market state (up, down, choppy).  
3. **Modeling:** Train a model to predict the regime 10 hours forward.  
4. **Signal generation:** Use model confidence to determine trade entries.  
5. **Risk management:** Adaptive stop-loss / take-profit based on volatility.

---

## 🎯 Goal
To build an interpretable, data-driven trading framework that links:
- **Technical indicators** (momentum, trend, volatility)
- **Sentiment and fundamental data**
- **Machine learning predictions**
  
into one unified strategy for the cryptocurrency market.

---

**And that’s it — good luck to us! 🚀**
