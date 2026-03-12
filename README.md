# Financial Ratio Quantile Strategy 
## Constructing & Optimizing Rank-Based Equity Portfolios
---
## Goal
We evaluate the efficacy of single-factor and multi-factor signals within a market-neutral, long-short equity framework. The project systematically backtests top-and-bottom decile trading strategies based on fundamental financial ratios to determine the primary drivers of alpha, concluding with an optimized weighted vigintile approach.

## Strategy Mechanics
* **Universe & Ranking:** Equities are cross-sectionally ranked and bucketed into quantiles (deciles and vigintiles) based on target financial ratios.
* **Factors Evaluated:**
  * **Value:** Price-to-Earnings (P/E) Ratio
  * **Quality:** Return on Investment (ROI)
  * **Safety:** Debt-to-Market Capitalization
* **Execution:** Market-neutral, long-short portfolio construction.
* **Rebalancing:** Monthly schedule to capture factor momentum and decay.
* **Cost of Capital:** Dynamic funding costs integrated using LIBOR/SOFR rates for accurate net-return modeling.

## Key Findings & Performance

### 1. The Dominance of Value
Across the sample period, the **Value factor (P/E Ratio)** served as the primary driver of returns, consistently outperforming Quality and Safety metrics in isolation.

### 2. Multi-Factor Composite
A composite signal targeting **High Debt / Low P/E / Low ROI** was constructed to test overlapping factor exposures. 
* **Result:** The composite expanded the pure return ceiling to **11.30%**, but introduced significantly higher portfolio volatility, highlighting the tradeoff between maximum theoretical yield and risk-adjusted stability.

### 3. Vigintile Optimization (The Extremes)
A Weighted Vigintile experiment was conducted to test the hypothesis that rank-based signals decay rapidly outside the absolute tails of the distribution.
* **Result:** The quantile ranking system is highly sensitive to concentration. By allocating capital exclusively to the **top 5%** of the P/E Ratio distribution, the strategy achieved its optimal performance:
  * **Peak Pure Return:** 12.15%
  * **Sharpe Ratio:** 1.41
