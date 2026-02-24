# State Demographics and Income Analysis (2021–2023)

## Overview

This project analyzes U.S. state-level demographic and economic data from 2021 to 2023.  
It integrates population data (by age and sex) with state-level median household income to explore cross-sectional differences across states.

The workflow includes data cleaning, preprocessing, feature engineering, and exploratory data analysis.

---

## Data Sources

- U.S. Census Bureau – State population data by age and sex  
- State-level median household income data (2021–2023)

Median household income is measured at the state–year level and merged onto demographic records for analysis.

---

## Requirements

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```
---

## How to run
### Option1: Jupyter Notebook
```bash
jupyter notebook
```
Open the main notebook and run all cells.

### Option2: Python Script
```bash
python main.py
```
(Adjust file name if different.)

---

## Limitations
- Income data is available only for 2021–2023.

- Income is measured at the state–year level and does not vary by age or sex.

- Analysis focuses on cross-sectional comparisons due to limited time span.

---

## Authors
Yao Ouyang, Zihan Chen, Jingyang Zhang

STATGR 5243 -- Columbia University
 
