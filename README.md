# Stock Analysis Engine with Machine Learning

A comprehensive Python-based financial analysis platform that combines traditional statistical analysis with advanced machine learning techniques for in-depth stock market insights.

## Features

### Traditional Financial Analysis
- **Statistical Metrics**: Historical Volatility, Skewness, Kurtosis, Sharpe Ratio
- **Return Analysis**: Logarithmic returns calculation and distribution analysis
- **Visualization Suite**: Professional-quality charts with matplotlib and seaborn
- **Multi-Stock Comparison**: Side-by-side statistical comparison

### Machine Learning Capabilities
- **Regression Analysis**: Pairwise regression models with beta coefficients and R² values
- **Correlation Analysis**: Static and rolling correlation matrices with heatmap visualizations
- **Cointegration Testing**: Engle-Granger tests for long-term relationship identification
- **Predictive Modeling**: Foundation for price prediction and portfolio optimization

### Advanced Visualizations
- Returns distribution plots with normal distribution overlay
- Rolling volatility trend analysis
- Correlation heatmaps with statistical significance
- Regression scatter plots with trend lines
- Time series correlation evolution



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

### ML Metrics
- **Beta Coefficient**: Stock's sensitivity to market movements (β > 1 = more volatile than market)
- **R-Squared**: Percentage of variance explained by the model (0-1 scale)
- **Correlation**: Linear relationship strength between two stocks (-1 to +1)
- **Cointegration**: Long-term equilibrium relationship between stock prices


##  Technical Implementation

### Data Source
- **Yahoo Finance API** via `yfinance` library
- Real-time and historical stock data
- Reliable day-end pricing information

### Core Libraries
- **pandas & numpy**: Data manipulation and numerical computations
- **scipy**: Advanced statistical calculations
- **scikit-learn**: Machine learning algorithms
- **statsmodels**: Econometric analysis and cointegration testing
- **matplotlib & seaborn**: Professional visualization

### Machine Learning Algorithms
- **Linear Regression**: For beta calculation and relationship modeling
- **Pearson/Spearman Correlation**: For relationship strength measurement
- **Engle-Granger Test**: For cointegration analysis
- **Rolling Window Analysis**: For time-varying correlation patterns



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
