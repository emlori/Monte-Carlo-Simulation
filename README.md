# Monte-Carlo Simulation of Investment Portfolio

This project implements a Monte Carlo simulation to model the behavior of an investment portfolio. It uses historical stock price data to generate future returns based on statistical simulations, helping assess portfolio performance and risk.

## Requirements

To run the project, the following Python libraries must be installed:

```bash
pip install yfinance plotly mpld3
```

## Code Overview

### 1. Data Loading

The code uses `yfinance` to load historical stock prices for a selection of stocks and indices. These prices include dividends and are retrieved for the period from January 1, 2023, to May 31, 2024.

- **Ticker List**: Stocks and indices from different sectors (e.g., RI.PA, SU.PA, ^SP500TR).
- **Data Filling**: Missing values due to non-trading days are forward-filled to handle `NaN` values.

### 2. Portfolio Returns Calculation

Daily portfolio returns are calculated based on predefined weights for each stock in the portfolio. This enables tracking the cumulative performance of the portfolio over time.

### 3. Monte Carlo Simulation

Monte Carlo simulations are used to model future portfolio returns by generating random daily returns based on historical statistics.

- **Number of Simulations**: 100 simulations of random portfolio returns are run.
- **Cumulative Returns**: Each simulation tracks the cumulative returns over time, and results are plotted to visualize potential future outcomes.

### 4. Value at Risk (VaR)

The code calculates the Value at Risk (VaR) at a 95% confidence level, providing a quantifiable measure of market risk.

- **VaR**: Indicates the potential loss in the portfolio over a given period with a certain confidence level.
- **Backtesting VaR**: Compares actual portfolio returns against the rolling VaR to identify breaches and validate the model's accuracy.

### 5. Visualizations

- **Portfolio Performance**: Plots cumulative portfolio returns over time.
- **Monte Carlo Simulations**: Visualizes simulated returns from multiple scenarios.
- **VaR Analysis**: Displays histograms of returns and rolling VaR over time.
  
### Key Insights

- **Risk Assessment**: VaR and Monte Carlo simulations help assess the portfolio's potential risk and performance.
- **Model Assumptions**: The simulation assumes normal distributions, which may not fully account for extreme market events.

## How to Run the Code

1. Ensure you have the required libraries installed.
2. Run the code in a Python environment, preferably a Jupyter notebook.
3. Explore the different visualizations to understand the potential risks and returns of the portfolio.

This simulation serves as a useful tool for investors to model risk and returns based on historical data and probabilistic scenarios.
