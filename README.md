

```
# Financial Data Preprocessing and Exploratory Data Analysis (EDA)

## Overview

This project focuses on the preprocessing and exploratory analysis of historical financial data for three key assets: Tesla (TSLA), Vanguard Total Bond Market ETF (BND), and S&P 500 ETF (SPY). The data, sourced using the YFinance API, spans from January 1, 2015, to October 31, 2024. Task 1 involves cleaning and preparing the data, performing initial analyses, and saving the cleaned datasets for use in forecasting and portfolio optimization.

## Objectives

- **Fetch Historical Data**: Extract historical price data using the YFinance library.
- **Data Cleaning**: Address missing values, outliers, and standardize data types for accurate analysis.
- **Exploratory Data Analysis (EDA)**: Conduct statistical and visual analysis to understand trends, volatility, seasonality, and risk.

## Dataset Details

Each dataset includes the following columns:
- **Date**: Trading day timestamp
- **Open, High, Low, Close**: Daily price metrics
- **Adj Close**: Adjusted close price, accounting for dividends and splits
- **Volume**: The total number of shares/units traded each day

### Asset-Specific Descriptions

- **TSLA**: A high-growth, high-risk stock in the consumer discretionary sector (Automobile Manufacturing)
- **BND**: A bond ETF that provides stability and income
- **SPY**: An ETF tracking the S&P 500 Index, offering broad U.S. market exposure

## Task Breakdown

### Step 1: Data Collection
- **Description**: Use YFinance to download historical data for TSLA, BND, and SPY.
- **File Locations**: Saved in `../data/raw/TSLA_data.csv`, `../data/raw/BND_data.csv`, and `../data/raw/SPY_data.csv`.

### Step 2: Data Cleaning
- **Basic Statistics**: Inspect data distribution, data types, and identify missing values.
- **Handling Missing Values**: Fill or interpolate missing values as needed.
- **Outlier Detection**: Detect and address significant anomalies in the datasets.
- **Normalization**: Normalize or scale the data to improve model compatibility.
- **Saving Cleaned Data**: Cleaned data is saved in `../data/raw/TSLA_cleaned_data.csv`, `../data/raw/BND_cleaned_data.csv`, and `../data/raw/SPY_cleaned_data.csv`.

### Step 3: Exploratory Data Analysis (EDA)
- **Visualizing Closing Prices**: Identify trends and patterns over time.
- **Volatility Analysis**: Calculate and plot daily percentage changes to observe volatility.
- **Rolling Statistics**: Calculate rolling means and standard deviations to understand short-term trends.
- **Seasonality and Trends**: Decompose each time series to extract trend, seasonal, and residual components.
- **Risk Metrics**: Calculate Value at Risk (VaR) and Sharpe Ratio for a risk assessment of Tesla’s stock.

## Key Insights
- **Trends**: Observations on long-term price direction for each asset.
- **Volatility**: Daily and rolling volatility trends to assess fluctuations.
- **Risk Assessment**: Insights into potential risk, including VaR and Sharpe Ratio calculations.

## How to Run

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Install Requirements**:
   Install the required packages using `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**:
   Open the Jupyter notebook and execute the cells to perform each step in Task 1.

4. **Output Files**:
   Cleaned data will be saved in the `../data/raw/` directory with filenames:
   - `TSLA_cleaned_data.csv`
   - `BND_cleaned_data.csv`
   - `SPY_cleaned_data.csv`

## Dependencies

- `yfinance`: For fetching financial data.
- `pandas`: Data manipulation and analysis.
- `matplotlib` and `seaborn`: Data visualization.
- `numpy`: Numerical operations.
- `statsmodels`: For time series decomposition.
  
## Directory Structure

```
project-root/
│
├── data/
│   └── raw/
│       ├── TSLA_data.csv
│       ├── BND_data.csv
│       ├── SPY_data.csv
│       ├── TSLA_cleaned_data.csv
│       ├── BND_cleaned_data.csv
│       └── SPY_cleaned_data.csv
│
├── notebooks/
│   └── Task_1_EDA.ipynb
│
└── README.md
```

## Future Tasks

Task 2 will involve building time series forecasting models to predict future stock prices for these assets, beginning with the cleaned data prepared in Task 1.

```

