# Financial Ratio Quantile Strategy 
## Constructing & Optimizing Rank-Based Equity Portfolios
We evaluate single and multi-factor signals in a market-neutral, long-short equity model. Backtesting top/bottom decile strategies on fundamental ratios identifies key profit drivers, yielding an optimized weighted vigintile approach.

## Strategy Mechanics
* **Universe & Ranking:** Equities are cross-sectionally ranked and bucketed into quantiles (deciles and vigintiles) based on target financial ratios.
* **Factors Evaluated:**
  * **Value:** Price-to-Earnings (P/E) Ratio
  * **Quality:** Return on Investment (ROI)
  * **Safety:** Debt-to-Market Capitalization
* **Execution:** Market-neutral, long-short portfolio construction.
* **Rebalancing:** Monthly schedule to capture factor momentum and decay.
* **Cost of Capital:** Dynamic funding costs integrated using LIBOR/SOFR rates for net-return modeling.

## Key Findings & Performance

### 1. Value Factor (P/E Ratio) Performance  
Across the sample period, the **Value factor (P/E Ratio)** served as the primary driver of returns, consistently outperforming Quality and Safety metrics in isolation.

### 2. Multi-Factor Composite
A composite signal targeting **High Debt / Low P/E / Low ROI** was constructed to test overlapping factor exposures. 
* **Result:** The composite expanded the pure return ceiling to **11.30%**, but introduced significantly higher portfolio volatility.

### 3. Vigintile Optimization (The Extremes)
A Weighted Vigintile experiment was conducted to test the hypothesis that rank-based signals decay rapidly outside the absolute tails of the distribution.
* **Result:** The quantile ranking system is highly sensitive to concentration. By allocating capital exclusively to the **top 5%** of the P/E Ratio distribution, the strategy achieved its optimal performance:
  * **Peak Pure Return:** 12.15%
  * **Sharpe Ratio:** 1.41
 
### Data Notice
> The historical fundamental and pricing data used to backtest these strategies was sourced from Zacks Fundamentals B. To comply with vendor licensing agreements, this proprietary dataset is excluded from the repository.
