# Quantitative Finance Projects

## Overview
This repository contains advanced quantitative finance projects showcasing expertise in **stochastic calculus, numerical methods, algorithmic trading, and risk management**. The projects focus on high-level computational finance techniques used in hedge funds, investment banks, and proprietary trading firms.

## Projects

### 1. **Advanced Option Pricing and Hedging**
#### Description
This project explores various techniques for pricing and hedging financial derivatives, including European and American options.

#### Methods Implemented
- **Black-Scholes Model (BSM):** Analytical solution for option pricing.
- **Monte Carlo Simulation:** Pricing options using Geometric Brownian Motion (GBM) with variance reduction techniques.
- **Binomial & Trinomial Trees:** Discrete-time option pricing, including early exercise for American options.
- **Finite Difference Methods:** Solving the Black-Scholes PDE using explicit, implicit, and Crank-Nicolson schemes.
- **Delta Hedging:** Implementing a self-financing hedging strategy with real-world market conditions.
- **Stochastic Volatility Models:** Extending to the **Heston model** for volatility skew analysis.

#### Code
- [`option_pricing.ipynb`](option_pricing.ipynb)
- [`finite_difference_solver.py`](finite_difference_solver.py)

---

### 2. **Quantitative Trading Strategy with Deep Learning**
#### Description
This project develops a machine learning-driven trading strategy optimized using reinforcement learning.

#### Methods Implemented
- **Data Acquisition:** Extracting stock price and order book data from Yahoo Finance and Quandl.
- **Time Series Forecasting:** Using **LSTM and Transformer models** for stock price prediction.
- **Reinforcement Learning:** Optimizing trade execution using **Deep Q-Networks (DQN) and PPO**.
- **Backtesting:** Validating performance using Backtrader, evaluating **Sharpe Ratio, Sortino Ratio, and Maximum Drawdown**.
- **Market-Making Strategies:** Optimizing trade execution speed using **parallelized C++ implementations**.

#### Code
- [`quant_trading.ipynb`](quant_trading.ipynb)
- [`rl_trading.py`](rl_trading.py)

---

### 3. **Stochastic Interest Rate Models and Yield Curve Construction**
#### Description
This project models interest rates using stochastic processes and applies them to yield curve construction.

#### Methods Implemented
- **Hull-White Model:** Simulating interest rates using mean-reverting processes.
- **Cox-Ingersoll-Ross (CIR) Model:** Pricing interest rate derivatives.
- **Yield Curve Construction:** Bootstrapping spot rates from market data.
- **Interest Rate Swap Pricing:** Calculating fair values of fixed-income derivatives.

#### Code
- [`interest_rate_modeling.ipynb`](interest_rate_modeling.ipynb)
- [`yield_curve_builder.py`](yield_curve_builder.py)

---

### 4. **Portfolio Optimization and Risk Management**
#### Description
This project focuses on constructing optimal investment portfolios while minimizing risk using modern portfolio theory and risk management techniques.

#### Methods Implemented
- **Mean-Variance Optimization:** Implementing Markowitz's efficient frontier.
- **Capital Asset Pricing Model (CAPM):** Estimating expected returns and beta.
- **Value at Risk (VaR) & Conditional VaR (CVaR):** Measuring potential portfolio losses.
- **Monte Carlo Simulations for Risk Assessment:** Stress testing different market conditions.
- **Risk Parity Portfolio Construction:** Equalizing risk contributions among assets.

#### Code
- [`portfolio_optimization.ipynb`](portfolio_optimization.ipynb)
- [`risk_management.py`](risk_management.py)

---

### 5. **Credit Risk Modeling and Default Prediction**
#### Description
This project builds models to assess the probability of default and credit risk exposure using statistical and machine learning techniques.

#### Methods Implemented
- **Logistic Regression & Decision Trees:** Predicting default probabilities.
- **Survival Analysis:** Estimating time to default using Cox proportional hazard models.
- **Credit Scoring Models:** Implementing Altman’s Z-score and Merton’s structural model.
- **Stress Testing:** Assessing credit risk under different economic scenarios.
- **Machine Learning for Credit Risk:** Using Random Forests, XGBoost, and Neural Networks.

#### Code
- [`credit_risk_modeling.ipynb`](credit_risk_modeling.ipynb)
- [`default_prediction.py`](default_prediction.py)

---

### 6. **High-Frequency Trading Strategy Implementation**
#### Description
This project explores algorithmic strategies used in high-frequency trading (HFT), focusing on low-latency execution and market microstructure analysis.

#### Methods Implemented
- **Market Microstructure Analysis:** Understanding bid-ask spread dynamics.
- **Order Flow Prediction:** Using machine learning to predict short-term price movements.
- **Execution Algorithms:** Implementing VWAP, TWAP, and Implementation Shortfall.
- **Latency Optimization:** Parallelizing order execution for millisecond-level decision making.
- **Statistical Arbitrage Strategies:** Pair trading and mean reversion analysis.

#### Code
- [`hft_strategy.ipynb`](hft_strategy.ipynb)
- [`execution_algorithms.py`](execution_algorithms.py)

---

## Requirements
Install dependencies using:
```bash
pip install numpy pandas scipy matplotlib tensorflow torch jax backtrader
```

For performance optimization, use C++ and parallel processing where applicable.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/quant-finance-projects.git
   cd quant-finance-projects
   ```
2. Run Jupyter notebooks or Python scripts:
   ```bash
   jupyter notebook option_pricing.ipynb
   ```
3. Modify parameters in Python scripts for different market conditions.

