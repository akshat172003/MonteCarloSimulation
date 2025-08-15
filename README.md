# Monte Carlo Portfolio Optimization Simulation

## Overview

This project implements a comprehensive Monte Carlo simulation for portfolio optimization using financial data from various asset classes including stocks, precious metals, and cryptocurrencies. The simulation analyzes historical data from 2015 to 2023 to determine optimal portfolio weights that balance risk and return.

## Features

- **Multi-Asset Portfolio Analysis**: Analyzes a diverse portfolio including:
  - Technology stocks (MSFT, GOOGL, TSLA, AMZN)
  - Entertainment stocks (GME, FUBO)
  - Cryptocurrency (BTC-USD)
  - Other assets (SMME, KEGS)

- **Monte Carlo Simulation**: Uses thousands of random portfolio weight combinations to explore the risk-return frontier

- **Portfolio Optimization Functions**:
  - Maximum Returns optimization
  - Minimum Risk optimization  
  - Risk-constrained optimization
  - Efficient frontier analysis

- **Data Visualization**: Generates plots showing:
  - Portfolio returns vs. risk scatter plots
  - Efficient frontier curves
  - Optimal portfolio weight distributions

## Data Sources

- **Yahoo Finance**: Historical price data from 2015-01-01 to 2023-10-16
- **Asset Classes**: Stocks, precious metals, and cryptocurrencies
- **Time Period**: 8+ years of daily price data

## Dependencies

```python
import datetime as dt
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from pandas_datareader import data as wb
import yfinance as yf
from scipy.optimize import linprog
from scipy import optimize
```

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd MonteCarlo
```

2. Install required packages:
```bash
pip install numpy pandas matplotlib pandas-datareader yfinance scipy
```

3. Open the Jupyter notebook:
```bash
jupyter notebook MonteCarloSimulationAkshat.ipynb
```

## Usage

1. **Data Loading**: The notebook automatically downloads historical price data for the specified assets
2. **Portfolio Analysis**: Run the simulation cells to generate portfolio optimization results
3. **Visualization**: View the generated plots to understand the risk-return characteristics
4. **Results**: Examine the optimal portfolio weights and performance metrics

## Key Functions

### Portfolio Optimization Functions

- `Max_returns(MeanReturns, PortfolioSize)`: Maximizes portfolio returns
- `Min_Risk(CovarReturns, PortfolioSize)`: Minimizes portfolio risk
- `Min_RiskConstr(MeanReturns, CovarReturns, PortfolioSize, R)`: Minimizes risk with return constraints

### Monte Carlo Simulation

The simulation generates thousands of random portfolio weight combinations to:
- Explore the full risk-return spectrum
- Identify the efficient frontier
- Find optimal portfolio allocations

## Results

The simulation provides:
- **Optimal Portfolio Weights**: Asset allocation percentages for different risk-return profiles
- **Efficient Frontier**: The optimal risk-return combinations
- **Performance Metrics**: Annualized returns and risk measures
- **Visual Analysis**: Charts showing portfolio performance characteristics

## Author

**Akshat** - Portfolio optimization and Monte Carlo simulation analysis

## License

This project is for educational and research purposes. Please ensure compliance with data usage terms from Yahoo Finance and other data providers.

## Disclaimer

This simulation is for educational purposes only. Past performance does not guarantee future results. Always consult with financial professionals before making investment decisions.

## Contributing

Feel free to submit issues, feature requests, or pull requests to improve this portfolio optimization tool.

