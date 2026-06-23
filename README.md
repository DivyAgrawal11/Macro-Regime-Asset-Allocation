# Global Macro & Asset Allocation Dashboard (Indian Markets)

## Overview
This quantitative finance project builds an interactive macroeconomic terminal that tracks Indian inflation (CPI), interest rates, and industrial production to classify the current economic regime (Expansion, Slowdown, Contraction, Recovery). It establishes a data-driven framework for tactical asset allocation between Indian equities (NIFTY 50) and fixed income (10Y Government Bonds).

## Core Architecture
* **Data Ingestion Pipeline:** Automated extraction of time-series macroeconomic data via the FRED API (`fredapi`) and market data via Yahoo Finance (`yfinance`).
* **Feature Engineering:** Calculation of Year-over-Year (YoY) momentum, 6-month moving average trend smoothing, and Yield Curve Spreads (10Y - 3M).
* **Regime Classification Logic:** A rule-based algorithm determining business cycle phases by analyzing the acceleration/deceleration of industrial growth against inflationary trends.
* **Interactive Visualization:** Dynamic plotting of market returns overlaid with macro regimes using `plotly`, designed for immediate pattern recognition.

## Strategic Allocation Framework
The model outputs specific portfolio adjustments based on current conditions:
* **Recovery:** Overweight High-Beta Equities
* **Expansion:** Overweight Quality Equities
* **Slowdown:** Underweight Equities, Overweight Short-Duration Bonds / Cash
* **Contraction:** Underweight Equities, Overweight Long-Duration Bonds

## Technology Stack
* Python 3.x
* `pandas` & `numpy` (Time-series structuring and calculations)
* `fredapi` (Macroeconomic data feed)
* `yfinance` (Equity data feed)
* `plotly` (Interactive visualizations)

## How to Run
1. Obtain a free API key from [FRED (Federal Reserve Economic Data)](https://fred.stlouisfed.org/).
2. Open the notebook in Google Colab (link provided above).
3. Paste your API key into the `FRED_API_KEY` variable in the data ingestion cell.
4. Run all cells sequentially.
