# MIE1622HW4---Asset-Pricing-with-Black-Scholes-and-Monte-Carlo-Simulation

This project implements and compares analytical and simulation-based methods for pricing European and Barrier options. The work combines the Black-Scholes model with one-step and multi-step Monte Carlo methods to evaluate accuracy, efficiency, and sensitivity to volatility.

## Methods
- **Black-Scholes Formula**: Closed-form pricing of European call and put options  
- **Monte Carlo (European)**:  
  - One-step MC simulates terminal asset prices directly  
  - Multi-step MC simulates full asset price paths, more suitable for path-dependent options  
- **Monte Carlo (Barrier Knock-In Option)**:  
  - Up-and-in barrier at $110  
  - Option activates only if barrier is crossed before expiration  

## Results
- **European Options**:  
  - Black-Scholes and one-step MC produced nearly identical results, confirming accuracy  
  - Multi-step MC less efficient for European options but valuable for path-dependent ones  
- **Barrier Options**:  
  - Prices were lower than European options since payoff depends on barrier activation  
  - Example: one-step MC Barrier put priced at 0.0 vs. European put at ~7.89  
- **Volatility Sensitivity**:  
  - Higher volatility increased both call and put values due to greater chance of barrier activation  
  - Lower volatility decreased values as activation became less likely  

## Key Insights
- One-step MC is best for European options; multi-step MC needed for Barrier options  
- Barrier options always have lower payoffs than standard European options  
- Monte Carlo results converge to Black-Scholes values when steps = 1 and sufficient paths are used  
- Approx. 30,000 paths (call) and 700,000 paths (put) were required for MC to match Black-Scholes within cents  

## Skills Demonstrated
- Option pricing under Black-Scholes and Monte Carlo frameworks  
- Handling path-dependent derivatives (Barrier options)  
- Sensitivity analysis with respect to volatility  
- Python implementation of stochastic simulations (NumPy, SciPy)  
- Critical evaluation of model efficiency and accuracy  
