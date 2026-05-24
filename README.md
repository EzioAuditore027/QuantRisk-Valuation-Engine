# Multi-Method Option Valuation & Risk Attribution Engine

A professional-grade quantitative finance framework designed for high-fidelity derivative pricing, model validation, and risk attribution. This repository bridges theoretical martingale pricing with real-world market calibration, benchmarking discrete-time models against continuous-time closed-form solutions.

Developed as a quantitative sandbox for applied Financial Statistics, this engine demonstrates the rigorous model validation standards required in tier-1 financial consulting and risk advisory.

## 🚀 Features & Architecture

This project is divided into distinct analytical phases, moving from theoretical pricing to live-market risk management:

* **Phase 1: The Valuation Engine**
  * **Black-Scholes-Merton:** Analytical benchmark for European options.
  * **Binomial Tree (CRR):** Discrete-time recursive approach (Sondermann) using the **Snell Envelope** for American early-exercise features.
  * **Monte Carlo Simulation:** Path-dependent stochastic modeling using Geometric Brownian Motion (GBM).
* **Phase 2: Market Calibration** 
  * Integrates with `yfinance` to fetch live spot prices, dynamically calculate annualized historical volatility ($\sigma$), and extract proxy risk-free rates ($r$) via Treasury yields.
* **Phase 3: Sensitivity Analysis (The Greeks) & Stress Testing**
  * Computes analytical first-order ($\Delta, \nu, \Theta, \rho$) and second-order ($\Gamma$) derivatives.
  * Performs non-linear stress tests simulating market crashes and volatility shocks.
* **Phase 4: Backtesting & Strategy Evaluation**
  * Evaluates historical "Fair Value" predictions against realized market payoffs to quantify model Alpha and directional bias.
* **Phase 5: Risk Mitigation & 3D Visualization**
  * Simulates a Delta-hedged "Protective Put" strategy.
  * Generates a comprehensive **3D Surface Plot** to visualize portfolio convexity and Theta decay across varying stock prices and times to maturity.

## 🧮 Mathematical Framework

The engine is built on the deterministic foundations of Investment Science (Luenberger) and the stochastic calculus of Martingale theory (Sondermann).

1. **The No-Arbitrage Principle:** Assumes a frictionless market where risk-neutral probabilities ($q$) ensure the discounted asset price is a **$Q$-Martingale**.
2. **The Snell Envelope:** Solves the optimal stopping problem for American options where the value at any node $i,j$ is:
   $$V_{i,j} = \max(\text{Intrinsic Value}, \text{Continuation Value})$$
3. **Stochastic Price Evolution:** Modeled under the continuous-time framework:
   $$dS_t = r S_t dt + \sigma S_t dW_t$$

## 🛠️ Installation & Usage

1. Clone the repository:
```bash
   git clone [https://github.com/yourusername/option-valuation-engine.git](https://github.com/yourusername/option-valuation-engine.git)
   cd option-valuation-engine# Multi-Method Option Valuation & Risk Attribution Engine

A professional-grade quantitative finance framework designed for high-fidelity derivative pricing, model validation, and risk attribution. This repository bridges theoretical martingale pricing with real-world market calibration, benchmarking discrete-time models against continuous-time closed-form solutions.

Developed as a quantitative sandbox for applied Financial Statistics, this engine demonstrates the rigorous model validation standards required in tier-1 financial consulting and risk advisory.

## 🚀 Features & Architecture

This project is divided into distinct analytical phases, moving from theoretical pricing to live-market risk management:

* **Phase 1: The Valuation Engine**
  * **Black-Scholes-Merton:** Analytical benchmark for European options.
  * **Binomial Tree (CRR):** Discrete-time recursive approach (Sondermann) using the **Snell Envelope** for American early-exercise features.
  * **Monte Carlo Simulation:** Path-dependent stochastic modeling using Geometric Brownian Motion (GBM).
* **Phase 2: Market Calibration** 
  * Integrates with `yfinance` to fetch live spot prices, dynamically calculate annualized historical volatility ($\sigma$), and extract proxy risk-free rates ($r$) via Treasury yields.
* **Phase 3: Sensitivity Analysis (The Greeks) & Stress Testing**
  * Computes analytical first-order ($\Delta, \nu, \Theta, \rho$) and second-order ($\Gamma$) derivatives.
  * Performs non-linear stress tests simulating market crashes and volatility shocks.
* **Phase 4: Backtesting & Strategy Evaluation**
  * Evaluates historical "Fair Value" predictions against realized market payoffs to quantify model Alpha and directional bias.
* **Phase 5: Risk Mitigation & 3D Visualization**
  * Simulates a Delta-hedged "Protective Put" strategy.
  * Generates a comprehensive **3D Surface Plot** to visualize portfolio convexity and Theta decay across varying stock prices and times to maturity.

## 🧮 Mathematical Framework

The engine is built on the deterministic foundations of Investment Science (Luenberger) and the stochastic calculus of Martingale theory (Sondermann).

1. **The No-Arbitrage Principle:** Assumes a frictionless market where risk-neutral probabilities ($q$) ensure the discounted asset price is a **$Q$-Martingale**.
2. **The Snell Envelope:** Solves the optimal stopping problem for American options where the value at any node $i,j$ is:
   $$V_{i,j} = \max(\text{Intrinsic Value}, \text{Continuation Value})$$
3. **Stochastic Price Evolution:** Modeled under the continuous-time framework:
   $$dS_t = r S_t dt + \sigma S_t dW_t$$

## 🛠️ Installation & Usage

1. Clone the repository:
```bash
   git clone [https://github.com/yourusername/option-valuation-engine.git](https://github.com/yourusername/option-valuation-engine.git)
   cd option-valuation-engine