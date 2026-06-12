# Bayesian Analysis of US Spot Bitcoin ETFs
## Overview
This project provides a rigorous Bayesian investigation into the market structure, return inference, and tracking efficiency of the first six US spot Bitcoin ETFs. Analyzing 596 days of trading data from January 2024 to May 2026, this research bypasses standard frequentist limitations to provide direct probabilistic answers regarding market dominance, return expectations, and tracking error variations.  
## Key Findings
- Regime Shift in Market Dominance: Modeled via a Beta-Binomial conjugate framework, the analysis proves that BlackRock's (IBIT) market dominance intensified over time, clearing a 70% daily volume share threshold on 99.7% of trading days in its second year.
- Tracking Efficiency: Utilized a scaled inverse chi-squared posterior under an improper Jeffreys prior to evaluate tracking error variance. Structural market hours (24/7 Bitcoin vs. 6.5-hour ETF windows) drove a baseline tracking error that overshadowed fee-based differences.
- Bayesian Return Inference: Applied Normal-InvGamma conjugate models and MCMC tracking regressions (using brms/Stan) to evaluate the Efficient Market Hypothesis, revealing structural tracking lags ($\beta = 0.932$) caused by overnight market dynamics.

## Technical Stack
- Language: R
- Modeling: brms (Stan) for Hamiltonian Monte Carlo sampling, LearnBayes
- Data Engineering: quantmod, dplyr, tidyr
- Diagnostics: bayesplot for trace plots, autocorrelation checks, and R-hat convergence validation  
