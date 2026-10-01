<div align="center">

# 🛡️ Quantitative Portfolio Risk & Tail-Risk Analytics
### *Multi-Asset Risk Modeling, Value-at-Risk (VaR) & Macro-Stress Testing (2016–2026)*

[![Open In Colab](https://img.shields.io/badge/Launch-Google_Colab-orange?style=for-the-badge&logo=googlecolab)](https://colab.research.google.com/github/TON_PSEUDO/TON_REPO/blob/main/risque_portefeuilles.ipynb)
[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Status](https://img.shields.io/badge/Analysis-Completed-brightgreen?style=for-the-badge)]()

---
</div>

> [!NOTE]
> **Executive Summary:** This quantitative research framework evaluates market risk, extreme tail loss (VaR), and structural resilience across three allocation strategies (**Conservative**, **Balanced**, **Dynamic**) over a 10-year market cycle.

---

## 📌 Allocation Framework

The model aggregates daily adjusted closing price data (`yfinance`) across global asset classes:

| Asset Class | Ticker | Name | Profile |
| :--- | :--- | :--- | :--- |
| **Global Equities** | `URTH` | MSCI World ETF | High Beta / Growth |
| **Eurozone Equities** | `EZU` | MSCI EMU ETF | Cyclical / Regional Exposure |
| **U.S. Fixed Income** | `AGG` | Core U.S. Aggregate Bond | Yield / Capital Preservation |
| **Commodities** | `GLD` | SPDR Gold Shares | Inflation Hedge / Non-Correlated |

### 🎯 Portfolio Strategies
* **🛡️ Conservative:** `70% AGG` | `15% URTH` | `5% EZU` | `10% GLD`
* **⚖️ Balanced:** `40% AGG` | `35% URTH` | `15% EZU` | `10% GLD`
* **🚀 Dynamic:** `10% AGG` | `55% URTH` | `25% EZU` | `10% GLD`

---

## 📊 Risk Dashboard & Analytics

| Risk Metric | Conservative 🛡️ | Balanced ⚖️ | Dynamic 🚀 |
| :--- | :---: | :---: | :---: |
| **Annualized Volatility** | `6.21%` | `9.86%` | `14.55%` |
| **1-Day Historical VaR (95%)** | `0.58%` | `0.87%` | `1.32%` |
| **1-Day Parametric VaR (95%)** | `0.62%` | `0.99%` | `1.46%` |
| **Max Drawdown (Peak-to-Trough)** | `-18.18%` | `-21.43%` | `-28.85%` |

---

## 🌩️ Crisis Stress-Testing

> [!WARNING]
> **Scenario 1 — Liquidity Shock (COVID-19 Crash | Feb 19 – Mar 23, 2020)**
> - **Conservative:** `-8.73%` *(Strong fixed-income buffer)*
> - **Balanced:** `-19.03%`
> - **Dynamic:** `-28.53%` *(Severe drawdown driven by global equity sell-off)*

> [!CAUTION]
> **Scenario 2 — Inflation & Rate Hike Shock (Full Year 2022)**
> - **Conservative:** `-12.40%` *(Bond duration risk materialized)*
> - **Balanced:** `-13.59%`
> - **Dynamic:** `-15.17%` *(Cross-asset correlation converged to 1)*

---

## 🔬 Quantitative Takeaways & Model Limitations

1. **Fat Tails vs. Normality:** Parametric VaR slightly overstates tail risk vs. Historical VaR due to non-normal return distributions (kurtosis) in asset daily returns.
2. **Breakdown of 60/40 Hedge (2022):** Fixed income (`AGG`) failed as a safe haven during rapid rate hikes, demonstrating macro-regime sensitivity.
3. **FX Exposure:** Tickers are USD-denominated without EUR currency hedging.

---

## ⚡ Quickstart

```bash
git clone [https://github.com/TON_PSEUDO/TON_REPO.git](https://github.com/TON_PSEUDO/TON_REPO.git)
cd TON_REPO
pip install -r requirements.txt
