# US-Hybrid-DSGE-LSTM

Real-time hybrid DSGE-LSTM forecasting model with financial frictions  
Paper: "A Hybrid DSGE-LSTM Approach to Macroeconomic Forecasting with Financial Frictions"  
(under review – Empirical Economics)

## Replication Package

This repository contains all data and code to fully replicate the results in the paper.

### Contents
- data/ – raw and cleaned quarterly U.S. data (2000Q1–2024Q4) + variable sources  
- dynare/ – DSGE model (.mod file) and estimation log  
- python/ – data cleaning script, LSTM training notebook, requirements  
- figures/ – Figure 1 (both panels) and Table 3 (as shown in the paper)

### Quick Start
```bash
# 1. Install requirements
pip install -r python/requirements.txt

# 2. Clean data
python python/01_clean_data.py

# 3. Estimate DSGE model
(open Dynare → run dynare/DSGE_FinancialFrictions.mod)

# 4. Train hybrid model & view results
(open python/02_train_hybrid_model.ipynb)
