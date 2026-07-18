# Stock Analysis Engine

A Python-based, command-line financial analysis tool that combines classic statistical analysis with econometric relationship modelling (correlation, linear regression, and cointegration) to explore historical stock data.

> **Note on "Machine Learning":** the relationship analysis is built with `scikit-learn` and `statsmodels` (linear regression, correlation, and the Engle-Granger cointegration test). There is no trained/saved model, neural network, or forecasting yet — those remain on the roadmap below.

## Features

### Traditional Financial Analysis
- **Statistical Metrics**: Historical Volatility, Skewness, Kurtosis, Sharpe Ratio (risk-free rate assumed to be 0)
- **Return Analysis**: Logarithmic returns calculation and distribution analysis
- **Visualization Suite**: Charts rendered with matplotlib and seaborn, saved as PNG files
- **Multi-Stock Comparison**: Side-by-side statistical comparison

### Relationship Analysis (scikit-learn & statsmodels)
- **Regression Analysis**: Pairwise linear regression between stock returns, with slope (labelled "beta"), R², correlation, and p-value
- **Correlation Analysis**: Static and 30-day rolling correlation matrices with heatmap visualizations
- **Cointegration Testing**: Engle-Granger tests for long-term relationship identification

### Visualizations
- Returns distribution plots with a normal distribution overlay
- Rolling volatility trend analysis
- Correlation heatmaps
- Regression scatter plots with best-fit lines
- Rolling correlation over time



## Project Structure

```
stock-analysis-engine/
├── README.md                     # This file
├── LICENSE.txt                    # MIT License
├── requirements.txt              # Python dependencies
├── main.py                      # Main application entry point
├── __init__.py                  # Package initialization
│
├── analysis/                    # Core financial analysis
│   ├── __init__.py
│   ├── financial_metrics.py    # Statistical calculations
│   └── test_metrics.py         # Testing module
│
├── utils/                       # Data handling utilities
│   ├── __init__.py
│   ├── data_fetcher.py         # Yahoo Finance data retrieval
│   └── data_validator.py       # Data quality validation
│
├── visualization/               # Charting and plotting
│   ├── __init__.py
│   ├── stats_visualizer.py     # Traditional financial charts
│   └── test_visualizer.py      # Visualization testing
│
├── ml/                         # Machine Learning module
│   ├── __init__.py
│   └── correlation_analyzer.py # ML correlation & regression analysis
│
└── output/                     # Generated files
    ├── plots/                  # Traditional analysis charts
    └── ml_plots/              # Machine learning visualizations
```



##  Statistical Metrics Explained

### Traditional Metrics
- **Historical Volatility**: Annualized standard deviation of returns (risk measure)
- **Skewness**: Asymmetry of return distribution (negative = more left tail risk)
- **Kurtosis**: Tail heaviness compared to normal distribution (higher = more extreme events)
- **Sharpe Ratio**: Risk-adjusted return measure (return per unit of risk)

### Relationship Metrics
- **Beta (regression slope)**: The slope of a pairwise regression between two stocks' returns. Note this is stock-vs-stock, not the textbook market-relative beta (no market benchmark is used by default).
- **R-Squared**: Fraction of variance explained by the regression (0-1 scale)
- **Correlation**: Linear relationship strength between two stocks (-1 to +1)
- **Cointegration**: Long-term equilibrium relationship between stock prices


##  Technical Implementation

### Data Source
- **Yahoo Finance** via the `yfinance` library
- Historical daily (day-end) stock data, downloaded fresh on each run
- Fetched data is cached in memory within a run to avoid duplicate downloads

### Core Libraries
- **pandas & numpy**: Data manipulation and numerical computations
- **scipy**: Statistical calculations (skewness, kurtosis, Pearson correlation)
- **scikit-learn**: Linear regression and R² scoring
- **statsmodels**: Cointegration testing (Engle-Granger)
- **matplotlib & seaborn**: Visualization

### Algorithms Used
- **Linear Regression**: For the pairwise regression slope and R²
- **Pearson Correlation**: For relationship strength and significance (p-value)
- **Engle-Granger Test**: For cointegration analysis
- **Rolling Window Analysis**: For time-varying (30-day) correlation and volatility



## Future Enhancements

### Planned ML Features
1. **LSTM Price Prediction**: Neural networks for price forecasting
2. **Portfolio Optimization**: Modern Portfolio Theory implementation
3. **Sentiment Analysis**: News and social media impact analysis
4. **RAG Integration**: Natural language query interface

### Advanced Analytics
1. **Options Pricing Models**: Black-Scholes implementation
2. **Risk Management**: VaR and CVaR calculations
3. **Backtesting Framework**: Strategy performance evaluation
4. **Real-time Data Streaming**: Live market analysis



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. Feel free to open a PR
