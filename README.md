# vic-nem-load-forecast

Short-term electricity load forecasting for Victoria (VIC1 region) of Australia's National Electricity Market

## Goal

Forecast half-hourly operational demand for VIC1, **48 half-hours (24 hours) ahead**, with a daily forecast origin of 06:00 Australia/Melbourne. Outputs are probabilistic (quantile forecasts), not just point estimates.

## Data

- **Demand & price:** AEMO aggregated price and demand for VIC1, Jan 2024 – Jun 2026 (5-minute resolution, resampled to 30-minute for modelling)

### Source

- AEMO aggregated price and demand: https://www.aemo.com.au/energy-systems/electricity/national-electricity-market-nem/data-nem/aggregated-data

## Considered Approach

1. Naive baselines (last week, yesterday, seasonal naive)
2. LightGBM with engineered features (the real benchmark)
3. LSTM / TFT for probabilistic forecasts via quantile loss
4. Evaluation: MAPE, MAE, RMSE 

## Repo layout

## Status - work in progress
