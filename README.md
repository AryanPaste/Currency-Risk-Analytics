# Corporate Currency Risk & VaR Analytics Engine

## Project Overview
This project is an end-to-end data analytics and risk modeling pipeline designed to evaluate corporate currency exposure. It pulls historical exchange rate data, performs exploratory data analysis (EDA) to determine volatility and correlation across major currency pairs, and leverages stochastic AI modeling (Monte Carlo simulations) to predict future price paths. The final output calculates the Value at Risk (VaR), providing a quantitative measure of potential financial loss over a 30-day horizon.

This project was developed as part of the IBM SkillsBuild Data Analytics with AI Academic Internship Program.

## Dataset
The project does not rely on a static, downloaded CSV file. Instead, it dynamically ingests real-time and historical financial market data using the `yfinance` API. 
*   **Source:** Yahoo Finance (via `yfinance` Python library)
*   **Features Extracted:** Daily Close prices 
*   **Currency Pairs Analyzed:** USD/INR, EUR/INR, GBP/INR
*   **Timeframe:** January 2022 to January 2024 (2 years of daily data)

## Technologies Used
*   **Python 3.x** (Core programming language)
*   **Jupyter Notebook** (Development environment and execution)
*   **yfinance** (Data extraction and API ingestion)
*   **Pandas & NumPy** (Data manipulation, log returns, and matrix operations)
*   **Matplotlib & Seaborn** (Exploratory Data Analysis and statistical visualization)
*   **SciPy** (Statistical distributions for stochastic modeling)

## Setup and Run Instructions
1. Clone this repository to your local machine.
2. Open a terminal or command prompt in the repository directory.
3. Install the required dependencies by running:
   `pip install -r requirements.txt`
4. Open the Jupyter Notebook:
   `jupyter notebook Aryan_CurrencyRiskAnalytics.ipynb`
5. Run all cells sequentially from top to bottom. The `yfinance` library requires an active internet connection to fetch the historical data during execution.

## Key Information & Analytics Workflow
1.  **Portfolio Ingestion:** Automatically retrieves multi-year FX data.
2.  **Exploratory Data Analytics (EDA):** Generates correlation heatmaps to identify diversification opportunities between the Dollar, Euro, and Pound against the Rupee.
3.  **Predictive Risk Modeling (AI Component):** Simulates 10,000 independent 30-day price paths using Geometric Brownian Motion.
4.  **Decision Intelligence:** Outputs a 95% Confidence Interval Value at Risk (VaR), translating raw statistical variance into a concrete business metric (maximum expected loss).