# A Comprehensive Study of Assortment Optimization with Substitution and Uncertainty: Introducing a Machine Learning Heuristic

Welcome to this Assortment Optimization repository! This project showcases the outcomes of my internship where we focused on solving *assortment optimization* challenges using machine learning (ML) techniques. The primary aim was to enhance retail assortment planning by addressing *assortment-based* and *stock-out-based substitutions*, while also incorporating *stochastic modeling* for robust decision-making.
This is the code repo for the [Comprehensive Study of Assortment Optimization with Substitution and Uncertainty paper](https://hal.science/hal-04182275)

## Key Features

- **ML Heuristic for Assortment Optimization:** we've developed an ML-based heuristic that suggests optimized assortments, taking into account potential stock-outs and assortment substitutions. The heuristic leverages ML techniques to maximize performance metrics, like minimizing the runtime (11 days runtime for 200 products using an exact algorithm against 1 hour for 10000 products).

- **Assortment & Stock-Out-Based Substitutions:** This repository presents strategies for efficiently substituting products to prevent stock-outs, thus ensuring customer satisfaction. The code and explanations in the research report illustrate how to implement these strategies within the assortment optimization process.

- **Stochastic Modeling for Robust Solutions:** To enhance the solution's resilience, we've explored the stochastic nature of assortment optimization. This approach introduces adaptability to uncertain demand scenarios, contributing to a more reliable assortment planning strategy.

## Contents

- `/Stochastic setting`: This directory contains code samples and scripts showcasing the implementation of the stochastic formulation of the problem. Here, both assortment based and stock-out based substitutions are taken into consideration.

- `/Deterministic/Assortment Based Substitution Formulation`: In this directory, you will find the code to implement an exact algorithm using Xpress Solver to solve the assortment problem taking into consideration only the assortment based substitution (in the deterministic case, stock-out based substitution doesn't make much sense).You will find some tests that were run to assess the formulation too.
   
- `/Deterministic/Our heuristic`:This directory contains the codes for the scoring algorithm described in the research paper, the ML algorithm and the final results consisting in the assortment chosen.

## Getting Started

To explore the code, solutions, and examples, feel free to clone this repository. You can access [the detailed research report](https://hal.science/hal-04182275) which contains a thorough exploration of the methodologies, experiments, and outcomes, offering a holistic view of the project from inception to results.

To use the codes, your dataset of products should contain the following:

-**demand**: the average demand value per consumer.

-**price**: the price of the product.

-**cost**: the inventory cost induced by the product.

-**volume**: the volume of each unit of the product.

-**$(\alpha_{ij})_{i, j \in N}$**: the assortment based substitution matrix.

-**$(\beta_{ij})_{i, j \in N}$**: the stock_out substitution matrix.

## Citation

If you find this work useful for your research or projects, please consider citing the research report:

```bibtex
@techreport{abir:hal-04182275,
  TITLE = {{A Comprehensive Study of Assortment Optimization with Substitution and Uncertainty: Introducing a Machine Learning Heuristic}},
  AUTHOR = {Abir, Harrasse},
  URL = {https://hal.science/hal-04182275},
  INSTITUTION = {{Mohammed VI polytechnic university}},
  YEAR = {2023},
  MONTH = Aug,
  KEYWORDS = {Assortment optimization ; stochastic ; assortment based substitution ; stock-out based substitution},
  PDF = {https://hal.science/hal-04182275/file/assort_opt_subs_stoch.pdf},
  HAL_ID = {hal-04182275},
  HAL_VERSION = {v1},
}
