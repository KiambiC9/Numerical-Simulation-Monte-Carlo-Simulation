# Task 1
- **(a)** Simulate \(M\) paths for the underlying using **Euler–Maruyama discretisation**, compute discounted payoff, and approximate the call price.  
- **(b)** Compare Monte Carlo prices for various \(M\) against the analytical **Black–Scholes value** (graphical illustration).  
- **(c)** Repeat using the **explicit GBM solution** for \(S_T\), avoiding discretisation error.

# Task 2
Additionally, the derivation of **generalized Black–Scholes PDE** (with stochastic variance).

# Task 3
Euler-Maruyama discretization of Heston Model. 
---
Simulate the paths of S and V.
Discretization using Euler-Maruyama discretization.
Compare the simulated distribution with a log-normal distribution using the simulated mean and variance.
Plot histograms on both linear and logarithmic scales to highlight differences in the tails.

# Task 4
# Asian Option Pricing (Monte Carlo & Control Variates)

This repository contains Python implementations for pricing **Asian average-strike call options** under the Black–Scholes model using **Monte Carlo simulation**.  
It also demonstrates the **control variate method** with a geometric-average strike option as control to drastically improve efficiency.
## 📂 Project Structure

- **`asian_option_crude.py`**  
  - Simulates asset paths under Geometric Brownian Motion using Euler discretization.  
  - Estimates the price of an **arithmetic average-strike Asian call option** via Monte Carlo.  
  - Reports price, standard error, and 95% confidence interval.

- **`asian_option_control_variate.py`**  
  - Extends the estimator by using the **geometric average-strike Asian call** as a control variate.  
  - Computes the analytic expectation of the geometric option under Black–Scholes.  
  - Estimates the optimal control variate coefficient \( \theta \).  
  - Reports variance reduction, price estimate, and 95% confidence interval.

- **`variance_comparison.py`**  
  - Compares MC vs control variate in terms of variance and accuracy.  
  - Computes the **percentage variance reduction**:
    \[
    \text{Reduction} = \frac{\text{Var}_{crude} - \text{Var}_{CV}}{\text{Var}_{crude}} \times 100
    \]

- **`experiments.py`**  
  - Explores the effect of varying:
    - Number of monitoring points \(N\)  
    - Number of simulations \(M\)  
    - Volatility \( \sigma \)  
  - Generates plots showing how **confidence intervals shrink** with larger \(M\).  
  - Demonstrates the **efficiency of the control variate method**.

## 📈 Results Summary

- **Variance Reduction**: ~99.94% (≈ 1,600× improvement in efficiency)



