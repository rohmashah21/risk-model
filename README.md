# Apple (AAPL) Stock Risk Analysis

An Excel-based financial risk analysis tool that calculates historical volatility, daily returns, and annualized risk metrics for Apple Inc. (AAPL) stock using real market data.

## Description

This project provides a comprehensive risk analysis of Apple stock by calculating key statistical metrics from historical price data. It helps investors, traders, and portfolio managers understand the stock's volatility patterns and risk characteristics.

The analysis covers stock price data from **April 2025 to April 2026**, calculating:
- Daily returns
- Volatility (standard deviation of returns)
- Annualized volatility
- Variance of returns

## Features

- **Daily Return Calculation** - Computes percentage change in stock price day over day
- **Statistical Analysis** - Calculates mean, variance, and standard deviation of returns
- **Volatility Measurement** - Quantifies stock price fluctuations
- **Annualized Volatility** - Projects daily volatility to annual terms
- **Risk Interpretation** - Provides practical insights for investment decisions
- **Educational Notes** - Includes explanations of what each metric means

## Excel Structure

### Worksheet: `risk analysis`

| Column | Description |
|--------|-------------|
| **A** | Date (trading days from April 2025 - April 2026) |
| **B** | Closing Price (AAPL stock price) |
| **C** | Daily Return (r) = (Price_t - Price_{t-1}) / Price_{t-1} |
| **D** | (r - mean)² - Squared deviation from mean |

### Key Metrics Calculated

| Metric | Formula | Interpretation |
|--------|---------|----------------|
| **Mean Return** | `=AVERAGE(C:C)` | Average daily return over the period |
| **Total Sum of Squares** | `=SUM(D2:D251)` | Sum of squared deviations |
| **Sample Size (n)** | `=COUNT(D2:D251)` | Number of trading days |
| **Variance** | `=H8/(H9-1)` | Spread of daily returns |
| **Daily Standard Deviation** | `=H10^(1/2)` | Stock moves up/down by ~1.5% from average |
| **Annualized Volatility** | `=H11*SQRT(H9)` | Yearly price fluctuation of ±23% |

## 🔧 Formulas Used

### Daily Return
Daily Return = (Today's Price - Yesterday's Price) / Yesterday's Price

text

### Variance (Sample)
Variance = Σ(r - mean)² / (n - 1)

text

### Standard Deviation
σ = √Variance

text

### Annualized Volatility
Annualized Volatility = Daily σ × √252

text
*Note: 252 represents typical trading days in a year*

## Key Findings

Based on the analysis of Apple stock data:

| Metric | Value | Interpretation |
|--------|-------|----------------|
| **Daily Standard Deviation** | ~1.5% | Apple's daily return typically moves up or down by 1.5% from its average |
| **Annualized Volatility** | ~23% | Over a year, Apple's price fluctuates within ±23% of its expected return |

## Who Benefits From This Analysis

### Investors
- Understand risk before making investment decisions
- Set realistic return expectations
- Compare risk across different stocks

### Options Traders
- Determine appropriate option pricing
- Calculate implied volatility
- Set position limits

### Portfolio Managers
- Assess portfolio risk exposure
- Make asset allocation decisions
- Set risk management parameters

## File Structure
project 2 (1).xlsx
└── risk analysis (worksheet)
├── Date column (April 2025 - April 2026)
├── Price column (AAPL closing prices)
├── Daily Return calculations
├── Squared deviations
└── Summary statistics section

text

## How to Use

1. **Open the Excel file** - Navigate to the `risk analysis` sheet

2. **Review the data** - Examine historical price and return patterns

3. **Check summary statistics** - Located in columns G-H:
   - Mean return
   - Total sum of squares
   - Sample size (n)
   - Variance
   - Daily standard deviation
   - Annualized volatility

4. **Interpret results** - Use the provided interpretations to understand risk levels

5. **Update data** (optional) - Add new price data to extend the analysis

## Sample Calculation Walkthrough
Day 1 Price: 194.27
Day 2 Price:196.98

Daily Return = (196.98 - 194.27) / 194.27 = 0.01395 (1.395%)
Mean Return = Average of all daily returns
Deviation = 0.01395 - mean
Squared Deviation = (deviation)²
Variance = Sum of all squared deviations / (n-1)
Daily σ = √variance = 0.015 (1.5%)
Annualized σ = 0.015 × √252 = 0.23 (23%)

text

## Limitations

- Based on historical data only (past performance doesn't guarantee future results)
- Assumes normal distribution of returns
- Doesn't account for market regime changes
- Ignores overnight gaps and intraday volatility
- Uses simple returns instead of log returns

## Potential Improvements

- Add log returns calculation for better statistical properties
- Include beta calculation relative to S&P 500
- Add Value at Risk (VaR) calculation
- Implement conditional volatility models (GARCH)
- Add volatility cones for historical context
- Include downside deviation and Sortino ratio
- Add rolling volatility calculation
- Create visual charts of volatility over time

## Educational Notes

### What is Volatility?
Volatility measures the degree of variation in a stock's price over time. Higher volatility means higher risk but also potentially higher returns.

### Why Annualize?
Different investment horizons require different risk metrics. Annualizing allows comparison across different assets and time periods.

### Interpretation of Results
- **σ = 1.5% daily** → On a typical day, Apple's return will be within ±1.5% of its average about 68% of the time
- **σ = 23% annual** → Over a year, Apple's return will be within ±23% of its expected return about 68% of the time

## 👤 Author

**Rohma Shah**
- GitHub: [@rohmashah21](https://github.com/rohmashah21)

## License

MIT License

Copyright (c) 2024 Rohma Shah

**Disclaimer**: This analysis is for educational purposes only. Past performance does not guarantee future results. Always conduct your own research before making investment decisions.
