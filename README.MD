# Risk Parity Portfolio Backtesting

## Overview
This repository contains a Python-based framework for constructing, backtesting, <br>
and evaluating a dynamic multi-asset risk parity portfolio.

Risk parity is a systematic portfolio construction approach that allocates capital <br>
such that each asset contributes equally to total portfolio risk. This methodology <br>
is widely used by hedge funds and institutional investors as a diversification <br>
and risk-management strategy, particularly in multi-asset portfolios.

The project implements a rolling, volatility-based risk parity strategy using <br>
futures data across major asset classes and evaluates performance using a <br>
comprehensive set of return, risk, and drawdown metrics.

---

## Strategy Description
The strategy follows a standard inverse-volatility risk parity approach:

1. Download and preprocess historical price data for multiple asset classes
2. Resample data to a monthly frequency
3. Compute asset returns
4. Estimate rolling asset volatility
5. Construct inverse-volatility weights
6. Normalize weights to ensure full capital allocation
7. Apply a one-period lag to weights to avoid look-ahead bias
8. Compute portfolio returns
9. Evaluate performance using risk-adjusted metrics

The resulting portfolio aims to balance risk contributions across assets rather <br>
than allocating capital equally.

---

## Asset Universe
At a minimum, the portfolio includes futures proxies for the following asset <br>
classes:

- S&P 500 (Equities)
- 10-Year US Treasuries (Fixed Income)
- Gold (Commodities)
- US Dollar Index (FX)

The framework is easily extensible to additional assets or alternative universes.

---

## Performance Evaluation
The portfolio is evaluated using the following metrics:

- Annualized mean return
- Annualized volatility
- Sharpe ratio
- Sortino ratio
- Calmar ratio
- Maximum drawdown
- Skewness
- Kurtosis

These metrics provide a comprehensive view of both return generation and downside <br>
risk characteristics.

---

## Methodological Notes
- Returns are computed using log returns
- Volatility is estimated using a rolling window
- Portfolio weights are lagged to prevent look-ahead bias
- Risk-free rate assumptions are applied consistently across metrics
- The analysis focuses on systematic, rules-based portfolio construction

---

## Visualizations
The analysis includes visualizations such as:

- Asset price and return series
- Rolling volatility estimates
- Portfolio weight dynamics
- Cumulative portfolio returns
- Drawdown curves

These plots are used to interpret portfolio behavior across different market <br>
regimes.

---

## Repository Structure
```text
├── data/               # Raw and processed data
├── notebooks/          # Jupyter notebooks for analysis and exploration
└── README.md

---

# Disclaimer
This project is for educational and research purposes only.
It does not constitute investment advice or a recommendation to trade any financial <br>
instrument.

---

# Author
Wayne Bartlet

Background in Economics and Data Science with interests in quantitative research, <br>
systematic trading strategies, and machine learning applications in finance.