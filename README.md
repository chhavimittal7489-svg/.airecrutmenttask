# .airecrutmenttask
This was a ML project we were suppose to do to get recruited in .ai club of our college. We were to clean data then train a model on the given dataset
Power Demand Analysis & Feature Engineering

Overview
This project focuses on analyzing and preparing a dataset for **power demand forecasting** by integrating multiple real-world data sources such as power consumption, weather data, and economic indicators.

The objective is to uncover key factors influencing electricity demand and engineer meaningful features for future machine learning models.

Dataset Description

Power Demand Data
- Hourly electricity demand (`demand_mw`)
- Time-based observations

Weather Data
Selected relevant features:
- Temperature  
- Precipitation  
- Relative Humidity  
- Sunshine Duration  

Economic Indicators
Filtered features:
- Urban Population  
- Rural Population  
- Electric Power Consumption (per capita)

Approach

Data Preprocessing
- Converted datetime columns using `pandas`
- Selected relevant columns to reduce noise
- Standardized column names for merging
  
Handling Missing Data
- Used **forward fill (`ffill`)**
- Justification:
  - Economic indicators change gradually over time
  - Prevents unrealistic fluctuations

 Data Integration
- Merged:
  - Economic data (yearly → datetime)
  - Weather data
  - Power demand data
- Ensured proper time alignment

Feature Engineering

Lag Features
Created time-dependent features:
- `lag_1` → demand 1 hour ago  
- `lag_6` → demand 6 hours ago  

because 
Electricity demand shows strong temporal dependency, making lag features highly informative.

Correlation Analysis
- Computed correlation matrix to identify important features  

Strong Correlation:
- Lag features  
- Temperature  
- Urban population  
- Rural population  
- Electric power consumption  

Weak Correlation:
- Precipitation  
- Sunshine duration  
- Relative humidity  

Dropped weak features to improve model performance

Key Insights
- Lag features are highly predictive  
- Temperature significantly impacts demand  
- Economic indicators influence long-term trends  
- Feature selection improves signal quality  

Tech Stack
- Python  
- Pandas  
- NumPy  

What This Project Demonstrates
- Data cleaning & preprocessing  
- Feature engineering for time-series data  
- Multi-source data integration  
- Analytical thinking using correlation  
- Avoiding data leakage  

Future Work
- Train ML models (Linear Regression, XGBoost, LSTM)  
- Time-series cross-validation  
- Hyperparameter tuning  
- Model deployment  

Why This Project Matters
Power demand forecasting is critical for:
- Grid stability  
- Energy efficiency  
- Sustainable planning 

Author
**Chhavi Mittal**
