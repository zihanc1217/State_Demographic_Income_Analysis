# State Demographics and Income Analysis (2021–2023)

## 1. Overview

This project analyzes U.S. state-level demographic and economic data from 2021 to 2023.  
It integrates population data (by age and sex) with state-level median household income to explore cross-sectional differences across states.

The objectives are to:
   1. Perform systematic data cleaning and preprocessing

   2. Engineer new features relating to demographic composition and income trends

   3. Explore cross-sectional and temporal patterns in state income

   4. Visualize distributions, compare states, and interpret relationships

The analysis is fully implemented in Python using pandas, numpy, and matplotlib, and documented in the accompanying notebook.
---

## 2. Data Sources

- U.S. Census Bureau – State population data by age and sex  
- State-level median household income data (2021–2023)

Median household income is measured at the state–year level and merged onto demographic records for analysis.

---

## 3. Requirements

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
## 4. Data Cleaning
### 4.1 Variable Standardization
- Renamed columns to lowercase with snake_case for uniformity

- Standardized state names to avoid mismatch when merging

- Converted year fields to integer type

### 4.2 Handling Missing Values
- Confirmed no missing values in state identifiers or year fields

- Validated that demographic aggregates align with Census totals

- Ensured all 50 states have income values for each year

### 4.3 Type Casting
- Population counts coerced to integers

- Income values coerced to numeric

- Year set as integer for sorting and grouping operations

These steps ensured the merged dataset was consistent, analyzable, and ready for feature engineering.

---

## 5. Exploratory Data Analysis
### 5.1 Income Distribution Across States
- Histogram of median incomes shows clear separation of high-income vs low-income states

- Mean income and skewness illustrate asymmetry in income distribution

- Identifies top income states versus states with structural disadvantages

![alt text](image.png)

### 5.2 Income Trends
- Line plots showing a clear upward trend in median household income from 2021 to 2023

- Income increases steadily across the three years, rising from approximately $68,000 in 2021 to about $76,500 in 2023

- From 2022 to 2023, income continues to rise but at a slightly slower pace, indicating a moderation in growth rather than a reversal

![alt text](image-1.png)


### 5.3 Correlation Analysis
- The correlation between state population and median household income is 0.135, indicating a weak positive linear association

- The skewness of −0.379 indicates a mild left-skew in the income distribution. This suggests the presence of a small number of relatively low-income states that extend the lower tail of the distribution

---

## 6. Feature Engineering
### 6.1 Age Group Aggregation
Age groups were consolidated into broader categories:

- 0–17: children and adolescents

- 18–64: working-age population

- 65+: older adults

These variables help analyze relationships between age structure and income patterns

### 6.2 Income Growth
This feature measures year-over-year percentage change in median income

- Growth rates were strongest between 2021 and 2022 and slowed slightly in 2023 for many states 

- Variability across states is non-negligible

- A few states show much higher volatility than the national average

![alt text](image-3.png)

### 6.3 Income volatility
 - High-income states do not necessarily exhibit higher relative volatility

 - Some mid-income states display disproportionate fluctuation

 - Several states show remarkably stable income trajectories across years

![alt text](image-2.png)

---

## 7. Key Insights
1. Income differences across states are large and persistent

2. States with higher proportions of working-age adults tend to report higher income levels

3. States with large elderly populations face growth challenges

4. With only three years of data, state income rankings show minimal volatility

5. Post-2021 patterns show uneven growth. Some states recovered faster than others

---

## 8. Technical Stacks and Skills Demonstrated
### Programming:
   - Python
   - Numpy, Pandas
   - matplotlib, seaborn

### Data Work:
   - Cleaning
   - Preprocessing
   - Merging multi-source datasets
   - Feature Engineering

### Data Analytics:
   - EDA
   - Correlation and interpretation
   - Data-driven insight extraction

### Communication:
   - Clear graphs
   - Structured, reproducible notebooks
   - Logical narrative describing findings

---

## Repo Structure
/
├── README.md
├── notebooks/
│   ├── 01_intro_data_feature.ipynb
│   ├── 02_preprocessing_feature_engineering.ipynb
│   └── 03_eda_visualization.ipynb
├── data/
│   ├── raw/
│   │   ├── population_dataset.csv
│   │   └── median_income_state.csv
│   └── processed/
│       ├── cleaned_merged_dataset.csv
│       └── merged_dataset.csv
└── outputs/
    └── Report.ipynb


- `notebooks/`
  - `01_intro_data_feature.ipynb` initial data exploration, variable understanding, and data cleaning 
  - `02_preprocessing_feature_engineering.ipynb` data cleaning, merging, and feature engineering  
  - `03_eda_visualization.ipynb` exploratory data analysis and visualizations  

- `data/`
  - `raw/` original demographic and income CSV files  
  - `processed/` merged dataset and cleaned merged dataset used in the analysis  

- `outputs/`
  - `Report.ipynb` final narrative style report summarizing methods and key findings

---

## Limitations
- Income data is available only for 2021–2023.

- Income is measured at the state–year level and does not vary by age or sex.

- Analysis focuses on cross-sectional comparisons due to limited time span.

 
