---
title: "R/Finance 2014:Complex Portfolio Optimization with PortfolioAnalytics"
author: Ross Bennett
date: May 16, 2014
output: beamer_presentation
toc: true
---

# Portfolio Optimization

## General
TODO: Add some general comments here about goals and pitfalls of optimizatio in the context of constructing a portfolio.

## Modern Portfolio Theory
"Modern" Portfolio Theory (MPT) was introduced by Harry Markowitz in 1952.

In general, MPT states that an investor's objective is to maximize portfolio expected return for a given amount of risk.

General Objectives

* Maximize a measure of gain per unit measure of risk
* Minimize a measure of risk
* Maximize a utility function

How do we define risk?

## Portfolio Optimization Objectives
* Minimize Risk
    * Volatility
    * Tail Loss (VaR, ES)
    * Other Downside Risk Measure
* Maximize Risk Adjusted Return
    * Sharpe Ratio
    * Modified Sharpe Ratio
    * Several Others
* Risk Budgets
    * Equal Component Contribution to Risk (i.e. Risk Parity)
    * Limits on Component Contribution
* Maximize a Utility Function
    * Quadratic, CRRA, CARA, etc.

# PortfolioAnalytics

## Overview

PortfolioAnalytics is an R package designed to provide numerical solutions and visualizations for portfolio problems with complex constraints and objectives.

## Key Features

* Support for multiple constraint and objective types
* Modular constraints and objectives
* An objective function can be any valid R function
* Custom moments
* Solver agnostic
* Visualizations

<!---
The key points to make here are:
- Flexibility
  - The multiple types and modularity of constraints and objectives allows us to add, remove, combine, etc. multiple constraint and objective types very easily.
  - Define an objective as any valid R function
  - Define a function to compute the moments (sample, robust, shrinkage, factor model, GARCH model, etc.)
- PortfolioAnalytics comes "pre-built" with several constraint types.
-->


## Support Multiple Solvers

Linear and Quadratic Programming Solvers

* R Optimization Infrastructure (ROI)
    * GLPK (Rglpk)
    * Symphony (Rsymphony)
    * Quadprog (quadprog)

Global (stochastic or continuous solvers)

* Random Portfolios
* Differential Evolution (DEoptim)
* Particle Swarm Optimization (pso)
* Generalized Simulated Annealing (GenSA)

## Workflow
TODO: Add a nice graphic here (Guy might have one)

Specify a Portfolio --> Add Constraints --> Add Objectives --> Run Optimization --> Analyze Results

# Examples

## Data
Here we will look at portfolio optimization in the context of portfolio of hedge funds

* EDHEC-Risk Alternative Indexes
* Monthly returns from 1/31/1997 to 1/31/2014
    * Convertible Arbitrage (CA)
    * CTA Global (CTAG)
    * Distressed Securities (DS)
    * Emerging Markets (EM)


## Monthly Returns



![](figure/unnamed-chunk-2.png) 


## Distribution of Monthly Returns
![](figure/unnamed-chunk-3.png) 



# Conclusion

## Acknowledgements
Many thanks to

* Google: funding for Google Summer of Code (GSoC)
* GSoC Mentors: Brian Peterson, Peter Carl, Doug Martin, and Guy Yollin
* R/Finance Committee

<!---
- One of the best things about GSoC is the opportunity to work and interact with the mentors.
- Thank the GSoC mentors for offering help and guidance during the GSoC project and after as I continued to work on the PortfolioAnalytics package.
- R/Finance Committee for the conference and the opportunity to talk about PortfolioAnalytics.
- Google for funding the Google Summer of Code for PortfolioAnalytics and many other proposals for R
-->



