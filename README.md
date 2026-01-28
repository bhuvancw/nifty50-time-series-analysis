# NIFTY 50 Time-Series Analysis

A comprehensive quantitative analysis of the NIFTY 50 Indian stock index spanning 10 years (2016-2026). This project explores key financial metrics including returns distribution, volatility dynamics, drawdown analysis, and market regime identification.

## 📊 Project Overview

This project conducts an in-depth time-series analysis of the NIFTY 50 index, one of India's primary stock market benchmarks. The analysis covers key aspects of market behavior and risk metrics essential for portfolio management and investment decision-making.

**Data Period:** January 2016 - January 2026 (2,477 trading days)

## 📁 Project Structure

### 1. **01_data_cleaning.ipynb**
   - **Purpose:** Data preparation and cleaning
   - **Key Steps:**
     - Load NIFTY 50 historical data from CSV
     - Parse and convert date columns to datetime format
     - Sort data chronologically (oldest to newest)
     - Convert price columns (Price, Open, High, Low) from string format to float
     - Handle volume data conversion (M for millions, B for billions)
     - Convert percentage changes to numeric format
   - **Output:** Clean dataset with 2,477 records and 7 columns (Date, Price, Open, High, Low, Vol., Change %)

### 2. **02_eda_returns.ipynb**
   - **Purpose:** Exploratory Data Analysis of returns and performance metrics
   - **Key Analyses:**
     - **Daily Returns Calculation:** Percentage change calculation for daily prices
     - **Return Statistics:** Mean (0.0543%), Std Dev (1.0175%), Range (-12.98% to +8.76%)
     - **Annualized Metrics:**
       - Annual Return: 13.68%
       - Annual Volatility: 16.15%
     - **CAGR (10-Year):** 12.91% compounded annual growth rate
     - **Return Distribution:** Histogram visualization to identify fat tails
     - **Yearly Performance Analysis:** Year-by-year return breakdown
     - **Best Year:** 2017 (28.65% return)
     - **Worst Year:** 2026 (-4.14% YTD, partial year)

### 3. **03_risk_volatility.ipynb**
   - **Purpose:** Risk assessment and volatility analysis
   - **Key Metrics:**
     - **Volatility Analysis:**
       - Annual Volatility: 16.15%
       - Sharpe Ratio: 0.475 (risk-adjusted returns, using 6% risk-free rate)
     - **Rolling Volatility:** 30-day, 90-day, and 252-day (annual) rolling windows
     - **Historical Volatility Patterns:** Peak volatility observed during market stress periods
       - Highest 252-day volatility: 31.93% (March 2, 2021)
     - **Risk Summary:** Comprehensive risk metrics in tabular format

### 4. **04_drawdown_regimes.ipynb**
   - **Purpose:** Maximum drawdown analysis and recovery patterns
   - **Key Metrics:**
     - **Maximum Drawdown:** -38.44% (worst peak-to-trough decline)
     - **Drawdown Timeline:** Most severe drawdown occurred March 2020 (COVID-19 pandemic period)
     - **Cumulative Returns:** Tracking wealth growth over 10 years
     - **Recovery Analysis:** Time to recovery from maximum drawdown (~7 days)
     - **Visualizations:** 
       - Underwater plot showing drawdown periods
       - Top 5 worst drawdown dates

### 5. **05_market_regime_analysis.ipynb**
   - **Purpose:** Market regime classification and regime-dependent performance
   - **Methodology:**
     - 90-day rolling returns threshold: >10% (Bull), <-10% (Bear), else Sideways
   - **Regime Distribution:**
     - Sideways: 1,696 days (68.4%)
     - Bull: 683 days (27.6%)
     - Bear: 98 days (4.0%)
   - **Regime Performance:**
     - **Bull Market:** Avg Daily Return +0.134%, Volatility 12.87%
     - **Sideways Market:** Avg Daily Return +0.032%, Volatility 13.72%
     - **Bear Market:** Avg Daily Return -0.123%, Volatility 46.74%
   - **Visualizations:** Scatter plot of index levels colored by market regime

## 📈 Key Findings

- **Long-term Growth:** NIFTY 50 has delivered a 12.91% CAGR over the 10-year period
- **Return Profile:** Average daily return of 0.0543% with moderate volatility of 1.0175%
- **Risk-Adjusted Returns:** Sharpe ratio of 0.475 indicates reasonable compensation for risk taken
- **Volatility Trends:** Volatility has fluctuated significantly, ranging from ~12% to ~32% over rolling windows
- **Maximum Drawdown:** The index experienced a severe -38.44% drawdown during the March 2020 market crash
- **Recovery Speed:** Despite severe drawdowns, the index recovered relatively quickly
- **Market Regimes:** The index spends majority of time (68.4%) in sideways consolidation phases
- **Regime Analysis:** Bear markets show significantly higher volatility (46.74%) compared to bull markets (12.87%)

## 📊 Data Files

- **Nifty 50 Historical Data - Original.csv:** Raw market data
- **Nifty 50 Historical Data - Cleaned.csv:** Preprocessed and cleaned data ready for analysis

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas:** Data manipulation and analysis
- **NumPy:** Numerical computations
- **Matplotlib:** Data visualization and charting

## 📝 Key Metrics Summary

| Metric | Value |
|--------|-------|
| Data Period | Jan 2016 - Jan 2026 |
| Total Observations | 2,477 trading days |
| CAGR | 12.91% |
| Annual Return | 13.68% |
| Annual Volatility | 16.15% |
| Sharpe Ratio | 0.475 |
| Maximum Drawdown | -38.44% |
| Best Year | 2017 (28.65%) |
| Worst Year | 2026 (-4.14% YTD) |

## 🎯 Use Cases

This analysis can be used for:
- Portfolio benchmarking against NIFTY 50
- Risk assessment and stress testing
- Understanding historical volatility patterns
- Market regime identification for tactical allocation
- Building quantitative trading strategies
- Academic research on Indian market dynamics

## 📌 Notes

- Analysis uses 252 trading days per year for annualized calculations
- Risk-free rate of 6% assumed for Sharpe ratio calculation
- Market regimes classified using 90-day rolling returns
- All calculations performed on adjusted closing prices

## 📄 License

This project is provided for educational and research purposes.
