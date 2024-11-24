

# Financial Derivatives Modeling

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![Last Commit](https://img.shields.io/github/last-commit/Frederik-Finance/financial-derivatives-modelling)

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technical Implementation](#technical-implementation)
  - [Part 1: Analytical Option Pricing](#part-1-analytical-option-pricing)
  - [Part 2: Model Calibration](#part-2-model-calibration)
  - [Part 3: Static Replication](#part-3-static-replication)
  - [Part 4: Dynamic Hedging](#part-4-dynamic-hedging)
- [Technologies Used](#technologies-used)
- [Repository Structure](#repository-structure)
- [Key Results](#key-results)
- [Skills Demonstrated](#skills-demonstrated)
- [Future Improvements](#future-improvements)
- [Academic Context](#academic-context)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Project Overview
The **Financial Derivatives Modeling and Risk Management** project offers a comprehensive implementation of financial derivatives pricing, calibration, and risk management strategies using Python. It encompasses various option pricing models, their calibration to real market data, and the analysis of hedging strategies for the S&P 500 index and related derivatives.

## Key Features
- **Multiple Option Pricing Models**: Implementation of Black-Scholes, Bachelier, Black, and Displaced-Diffusion models.
- **Model Calibration**: Calibrates models using real market data from the S&P 500 (SPX) and SPDR S&P 500 ETF (SPY).
- **Static Replication Strategies**: Develops strategies for exotic derivatives through static replication.
- **Dynamic Delta Hedging Simulation**: Simulates dynamic delta hedging with comprehensive error analysis.
- **Volatility Surface Modeling**: Constructs and analyzes detailed volatility surfaces.

## Technical Implementation

### Part 1: Analytical Option Pricing
- **Implemented Models**: Four major option pricing models.
- **Supported Option Types**:
  - Vanilla Calls/Puts
  - Digital Cash-or-Nothing Options
  - Digital Asset-or-Nothing Options
- **Model Validation**: Ensures consistency through cross-model comparisons.

### Part 2: Model Calibration
- **Calibration Period**: December 1, 2020.
- **Underlying Assets**:
  - SPX Index (3662.45)
  - SPY ETF (366.02)
- **Volatility Models**:
  - **Displaced-Diffusion Model**: Parameters σ (volatility) and β (displacement).
  - **SABR Model**: Parameters α, β, ρ, and ν.
- **Implied Volatility Surfaces**: Generation and analysis based on calibrated models.

### Part 3: Static Replication
- **Replication Strategies**: Static replication for exotic derivatives.
- **Complex Payoff Structures**:
  - Non-linear payoff function: \( S^{1/3} + 1.5 \times \log(S) + 10.0 \)
  - Model-free integrated variance.
- **Model Comparison**: Evaluates replication results across different pricing models.

### Part 4: Dynamic Hedging
- **Delta Hedging Strategy**: Implements Black-Scholes delta hedging.
- **Hedging Error Analysis**:
  - Utilizes 50,000 simulation paths.
  - Tests rebalancing frequencies of 21 and 84 times per month.
- **Visualization**: Displays hedging error distributions for analysis.

## Technologies Used
- **Programming Language**: Python 3.x
- **Libraries**:
  - **Numerical Computations**: NumPy, SciPy
  - **Data Manipulation**: Pandas
  - **Visualization**: Matplotlib, Seaborn
  - **Development Environment**: Jupyter Notebooks

## Repository Structure
```
├── notebooks/
│   ├── part1_analytical_pricing.ipynb
│   ├── part2_model_calibration.ipynb
│   ├── part3_static_replication.ipynb
│   └── part4_dynamic_hedging.ipynb
├── data/
│   ├── SPX_options.csv
│   ├── SPY_options.csv
│   └── zero_rates_20201201.csv
├── report/
│   └── report.pdf
├── requirements.txt
└── README.md
```

## Key Results
- **Market Price Replication**: Successfully replicated market option prices using calibrated models.
- **Static Replication Effectiveness**: Demonstrated the effectiveness of static replication strategies for exotic derivatives.
- **Hedging Error Quantification**: Quantified hedging errors under varying rebalancing frequencies.
- **Volatility Surface Analysis**: Analyzed the impact of model parameters on implied volatility surfaces.

## Skills Demonstrated
- **Quantitative Finance**
- **Financial Mathematics**
- **Stochastic Modeling**
- **Risk Management**
- **Python Programming**
- **Data Analysis**
- **Financial Markets Knowledge**

## Future Improvements
- **Exotic Options Expansion**: Implement additional exotic option types.
- **Enhanced Visualization**: Develop more sophisticated visualizations for risk metrics.
- **Real-Time Data Integration**: Incorporate real-time data feeds for dynamic analysis.
- **Performance Optimization**: Optimize code for large-scale simulations and faster computations.

## Academic Context
This project was completed as part of the **QF620 Stochastic Modelling in Finance** course, demonstrating the practical applications of financial theory in real-world market scenarios.

## Installation

### Prerequisites
- **Python**: Version 3.x
- **Package Manager**: pip

### Steps
1. **Clone the Repository**
   ```bash
    git clone https://github.com/Frederik-Finance/financial-derivatives-modelling.git
    cd financial-derivatives-modelling
   ```

2. **Create a Virtual Environment (Optional but Recommended)**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running the Notebooks
Open the Jupyter Notebooks located in the `notebooks/` directory using Jupyter Notebook or JupyterLab.

```bash
jupyter notebook
```

### Generating the Report
After running all parts, generate the comprehensive report located in the `report/` directory.

### Data Preparation
Ensure that the necessary data files are placed in the `data/` directory. If additional data is required, update the paths accordingly in the notebooks.

## License
This project is licensed under the [MIT License](LICENSE). It is available for academic and research purposes. Please cite appropriately if using any part of this work.

