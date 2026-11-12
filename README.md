# SMT Divergence Trading Strategy

**Status: Work in Progress (no alpha found)**

A quantitative trading research project focused on identifying and evaluating Smart Money Technique (SMT) divergences across correlated equity index futures. The goal is to develop a systematic, data-driven trading strategy through historical backtesting, realistic execution modeling, and iterative optimization.

## Overview

SMT divergence occurs when correlated markets exhibit differences in price behavior. For example, one index may establish a new high while another fails to do so, potentially indicating a weakening trend or an upcoming reversal.

This project investigates whether these divergences provide statistically meaningful trading opportunities.

The strategy monitors four equity index futures:

| Futures | Index | Micro Contract |
|---|---|---|
| ES | S&P 500 | MES |
| NQ | Nasdaq-100 | MNQ |
| YM | Dow Jones Industrial Average | MYM |
| RTY | Russell 2000 | M2K |

## Strategy Development

The current implementation uses Python to identify SMT divergence signals, evaluate potential trade entries, and simulate trade execution.

The research framework includes:

- **Signal generation:** Identifying divergences between correlated futures using historical price movements.
- **Market filters:** Evaluating correlation, relative trends, and divergence strength.
- **Trade execution:** Simulating entries, stop-losses, profit targets, and time-based exits.
- **Risk management:** Position sizing based on stop-loss distance, portfolio equity, and estimated futures margin requirements.
- **Performance evaluation:** Measuring profitability, drawdowns, win rates, and transaction costs.

## Data and Backtesting

Historical market data is sourced from Databento.

| Component | Implementation |
|---|---|
| Data provider | Databento |
| Markets | ES, NQ, YM, RTY |
| Signal timeframe | 5-minute |
| Execution timeframe | 1-minute |
| Trading session | 9:30 AM – 4:00 PM ET |
| Historical sample | November 2025 – October 2026 |
| Backtesting | Python |

The backtesting framework models transaction costs, execution delays, and slippage. Historical data is cleaned and synchronized across markets, with incomplete trading sessions and identified futures rollover periods excluded from the initial analysis.

## Strategy Optimization

The project is currently undergoing iterative optimization.

An AI-assisted research workflow is being developed to experiment with incremental changes to trading rules while preserving SMT divergence as the underlying strategy.

The optimization process focuses on improving entry and exit conditions, evaluating market filters, and testing performance across different market environments.

To reduce overfitting, historical data is divided chronologically into development, validation, and out-of-sample testing periods.

## Future Development

- [x] Develop initial SMT divergence detection logic
- [x] Implement historical backtesting
- [x] Integrate Databento futures data
- [x] Add transaction costs and margin-aware position sizing
- [ ] Evaluate optimized strategy variations
- [ ] Conduct out-of-sample performance testing
- [ ] Integrate Interactive Brokers for real-time data
- [ ] Implement automated paper trading
- [ ] Evaluate readiness for live execution

## Technologies

**Python**, pandas, NumPy, Jupyter Notebook, Databento, and Git.

Interactive Brokers API integration is planned for future development.

## Disclaimer

This project is for research and educational purposes. The strategy is experimental and has not demonstrated consistent profitability. Historical simulations do not guarantee future performance, and no live trading results are claimed.
