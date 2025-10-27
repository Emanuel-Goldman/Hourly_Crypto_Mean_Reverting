# Hourly Crypto Momentum Strategy

## Current Status & Next Steps

This project is **in active development**.

So far, the research has **found empirical evidence of mean-reverting behavior** in cryptocurrency prices.  
A **directional prediction model** has been successfully developed to estimate short-term price direction based on technical indicators.  

### 🔜 Next Steps
The next phase focuses on **converting model outputs into tradeable signals**, integrating confidence thresholds, and constructing a **signal-based trading framework** with backtesting and risk control.

---

## Overview

This project builds and tests an **algorithmic trading strategy** for the **cryptocurrency market**.  
The goal is to determine whether technical, sentiment, and fundamental indicators contain **predictive power** for short-term market direction — and to use those predictions to design profitable trading signals.

---

## Data

- **Source:** Top 100 market-cap cryptocurrencies from Binance  
- **Frequency:** Hourly OHLCV candles (`open`, `high`, `low`, `close`, `volume`)  
- Additional features include **momentum**, **RSI**, **MFI**, and other technical indicators engineered from historical data

---

## Project Structure

### **A. Data and Feature Engineering**

- `A_Data_Preprocessing.ipynb` — Loads and cleans raw hourly data  
- `B_MAD_Indicator.ipynb` — Tests **Moving Average Distance (MAD)** for predictive power, inspired by *Avramov, Kaplanski & Subrahmanyam (2018)*  
- `C_RSI_Indicator.ipynb` — Builds and evaluates **RSI-based features** across multiple time horizons  
- `D_Volume_Indicators.ipynb` — Derives **volume-driven indicators** such as MFI and volume z-scores  
- `E_Feature_Engineering.ipynb` — Combines all engineered indicators into a single modeling dataset

### **B. Modeling**

- `F_RF_Direction_Model.ipynb` — Trains a **Random Forest direction model** to predict the probability of upward or downward price movement  
  - Empirically confirms **mean-reverting dynamics** in short to medium horizons (24–168 hours)  
  - Produces **model probabilities** used for further signal generation

### **C. Strategy Layer**

- `H_Final_Strategy.ipynb` — *(In progress)*  
  - Converts model probabilities into **confidence-weighted trading signals**  
  - Implements filters for volatility, regime detection, and position sizing  
  - Prepares the framework for **backtesting and performance evaluation**

---

## Methodology Summary

1. **Feature Discovery** — Identify indicators with statistical or predictive significance  
2. **Labeling** — Define future returns and binary direction labels  
3. **Modeling** — Train ML models to capture directional patterns and mean reversion  
4. **Signal Generation** — Use model confidence to generate tradeable buy/sell signals  
5. **Evaluation** — Test predictive power and profitability across different horizons

---

## Goal

To build a **data-driven, interpretable trading framework** that combines:

- **Technical indicators** (momentum, volatility, volume)  
- **Empirical mean-reversion behavior**  
- **Machine learning–based directional forecasts**

into a unified **signal-generation and strategy execution system** for cryptocurrency markets.
