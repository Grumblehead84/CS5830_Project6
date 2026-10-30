# Project 6: Multiple Linear Regression on RRCA Baseflow Data

**CS 5830**

Kevin Shaffer & Ethan

## Overview

This project uses multiple linear regression to analyze how irrigation pumping, precipitation, and evapotranspiration affect observed baseflow in the Republican River Basin. Using data from the Republican River Compact Administration (RRCA) groundwater model, we build an OLS regression model with interaction terms and segment fixed effects to predict baseflow and derive climate-adaptive safe pumping thresholds.

## Dataset

- **Source:** RRCA groundwater model
- **Records:** 15,591 observations across 42 river segments
- **Variables:** Irrigation Pumping, Precipitation, Evapotranspiration, Observed Baseflow, Date, Segment ID, coordinates (x, y)

## Methods

- Multiple linear regression (OLS) via statsmodels and scikit-learn
- Interaction terms: Pumping × Precipitation, Pumping × ET
- 42 segment dummy variables to control for spatial differences
- 80/20 train-test split for validation

## Key Results

- **R² = 0.81** — the model explains 81% of the variation in baseflow
- **Test R² = 0.80**, RMSE = 25.36 — strong generalization to unseen data
- Pumping has a large negative effect on baseflow (coefficient = −5.11)
- Safe pumping thresholds vary by climate conditions rather than being a single fixed limit


## References

Xu, T. et al. (2015). "Estimation of groundwater recharge and baseflow using a coupled surface water–groundwater model." *Computational Geosciences*.