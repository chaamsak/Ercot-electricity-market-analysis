# ERCOT Electricity Market Analysis

## Overview
This project analyzes ERCOT electricity market data to identify load patterns, price behavior, price volatility trends, and generation mix changes over time. The workflow uses Python (Google Colab) for cleaning/aggregation and Power BI for visualization.

## Data Sources
- ERCOT Native Load (hourly system load)
- ERCOT Settlement Point Prices (RPT)
- ERCOT Generation by Fuel (IntGenbyFuel)

## Tools
- Python (pandas, numpy)
- Google Colab
- Power BI

## Methodology
- Cleaned and standardized ERCOT Excel datasets (multi-sheet, inconsistent headers)
- Aggregated:
  - Hourly load → monthly average load
  - 15-min prices → monthly average and volatility (std)
  - Generation by fuel → monthly totals and renewable share
- Built a Power BI dashboard to communicate results

## Outputs
- `data/processed/load_hourly_clean.csv`
- `data/processed/load_monthly_clean.csv`
- `data/processed/prices_monthly_clean.csv`
- `data/processed/generation_monthly_clean.csv`
- Power BI dashboard: `powerbi/ERCOT_Electricity_Market_Analysis.pbix`
- Dashboard screenshot: `visuals/dashboard_overview.png`
- Cleaning notebook: `notebooks/ercot_data_cleaning.ipynb`

## Key Insights (current version)
- ERCOT load shows an upward trend across the analyzed period
- Prices fluctuate year-to-year and may be negative during oversupply periods
- Price volatility varies over time
- Renewables increase gradually while natural gas remains dominant

## Next Steps
- Add seasonal analysis (Winter/Spring/Summer/Fall) by year
- Hub-level price comparisons
- Weather correlation analysis and baseline forecasting
