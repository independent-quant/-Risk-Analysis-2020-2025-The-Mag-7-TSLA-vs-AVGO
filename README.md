# [Risk Analysis 2020-2025] The "Mag 7" & TSLA vs AVGO

Link **[Google Colab](https://colab.research.google.com/github/independent-quant/-Risk-Analysis-2020-2025-The-Mag-7-TSLA-vs-AVGO/blob/main/mag7_analysis.ipynb)**

## Abstract

This repository contains a quantitative risk analysis of the "Magnificent 7" stocks (AAPL, MSFT, GOOGL, AMZN, NVDA, META, TSLA). Specifically, it examines the idiosyncratic risk of **Tesla (TSLA)** and tests a hypothesis of replacing it with **Broadcom (AVGO)**.

## Key Findings

### 1. Correlation Decoupling
Using a **126-day rolling correlation** against the S&P 500 (SPY), the analysis identifies a divergence:
*   **The Cluster:** Most Mag 7 components maintain a correlation > 0.6.
*   **The Outlier:** TSLA frequently decouples, with correlation dropping below 0.3, exhibiting behavior distinct from the "Big Tech" beta.

### 2. Risk Contribution
In an Equal-Weight portfolio, risk is concentrated:
*   **TSLA** contributes **>20%** of the total specific risk of the basket.
*   **AVGO**, by comparison, aligns closer to the volatility profile of the broader group.

### 3. Backtest Results (The "Swap")
A historical backtest (2020-2025) comparing the Classic Mag 7 against a Modified Basket (Ex-TSLA, +AVGO) yielded:
*   **Sharpe Ratio:** Improved from **0.77** to **0.79**.
*   **Max Drawdown:** Reduced from **-56.3%** to **-51.1%**.

### 4. Minimum Volatility Optimization
A Mean-Variance Optimization targetting **Minimum Volatility** (with L2 Regularization) allocated:
*   **0%** to TSLA (rejected due to volatility).
*   **Significant allocation** to MSFT, AAPL, and AVGO (favored for stability).

---

## Dependencies
*   `yfinance` (Data Aquisition)
*   `PyPortfolioOpt` (Efficient Frontier & Risk Models)
*   `plotly` (Interactive Visualizations)
*   `pandas` / `numpy`

## Usage
1.  Clone the repository.
2.  Install requirements: `pip install yfinance PyPortfolioOpt plotly`
3.  Run the notebook `mag7_analysis.ipynb`.

---
*Disclaimer: This project is for educational purposes only and does not constitute financial advice.*
