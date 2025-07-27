# 📉 Pair Trading Strategy – US Tech Stocks (2019–2023)

This project explores **statistical arbitrage** through a **pair trading strategy** using cointegrated stocks from the **US IT sector**. The method identifies pairs with strong cointegration and trades based on spread mean-reversion using Z-score thresholds.

---

## 🔍 Project Highlights

- **Stocks Used**: TSLA, AMZN, AAPL, GOOGL, MSFT, ORCL, CRM, IBM, ACN, NOW
- **Period**: Jan 2019 – Dec 2023
- **Techniques**:
  - OLS regression to compute hedge ratio
  - Z-score of residual spread as trading signal
  - Long/short signal generation based on deviation thresholds
- **Libraries**: `yfinance`, `pandas`, `numpy`, `statsmodels`, `matplotlib`, `sklearn`

---

## ⚙️ Strategy Logic

1. **Download price data** for selected tech stocks using `yfinance`.
2. **Test for cointegration** between all 45 possible pairs using `coint`.
3. **Select the most cointegrated pair** based on p-values.
4. **Trade logic**:
   - Go **long** if Z-score < -1
   - Go **short** if Z-score > +1
   - **Exit** when Z-score returns to 0

---

## 📈 Backtest & Evaluation

- Simulated trades executed using the above strategy on selected pairs.
- Performance visualized with spread plots, Z-score thresholds, and trade entry/exit points.
- Metrics like **cumulative return**, **drawdowns**, and **spread stationarity** included.

---

## 🖼️ Visualizations

- Price chart of selected pair
- Beta-adjusted spread with Z-score overlays
- Signal markers for trade entries/exits

---

## 📁 File

- `Pairtradingstrategy.ipynb`: Full implementation of the strategy in a Jupyter notebook.

---


## ⭐ Acknowledgements

- Strategy inspired by quant research methods and statistical arbitrage literature.
