# GMF Investments: Time Series Forecasting for Portfolio Optimization

## Project Overview

This project develops and validates a quantitative investment strategy for GMF Investments. It leverages time series forecasting (ARIMA) on high-growth assets (Tesla - TSLA) and integrates the results into a Modern Portfolio Theory (MPT) framework to optimize a portfolio also containing a broad market ETF (SPY) and a bond ETF (BND). The final strategy is backtested against a traditional 60/40 benchmark to prove its viability.

## Folder Structure

- **/data/processed/**: Contains the cleaned CSV files for each asset after initial preprocessing.
- **/notebooks/**: Contains the Jupyter notebooks detailing the step-by-step analysis.
  - `1_Data_Preprocessing_and_EDA.ipynb`: Data loading, cleaning, and exploratory analysis.
  - `2_Time_Series_Forecasting_Models.ipynb`: Development and comparison of ARIMA and LSTM models.
  - `3_Forecasting_and_Portfolio_Optimization.ipynb`: Forecasting, portfolio optimization, and backtesting.
- **/results/**: Contains the outputs of the analysis.
  - `/metrics/`: Text files with model performance metrics and the final portfolio summary.
- **/scripts/**: Contains any reusable Python scripts (e.g., for automated data fetching).

## How to Run

1.  Ensure you have Python 3.8+ installed.
2.  Install the required libraries:
    ```bash
    pip install yfinance pandas numpy matplotlib seaborn statsmodels pmdarima tensorflow scikit-learn
    ```
3.  Run the Jupyter notebooks in sequential order, starting with `1_Data_Preprocessing_and_EDA.ipynb`.

## Key Findings

- The model-driven strategy recommends a portfolio of **45.3% TSLA, 1.2% BND, 53.5% SPY**.
- In a one-year backtest (Aug 2024 - Jul 2025), the strategy achieved a **22.85% return** compared to the benchmark's **9.75%**.
- The project validates the potential of using forecasting models as a core component of GMF's portfolio management process.
