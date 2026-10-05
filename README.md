# Sales Forecasting Dashboard (Python + Power BI)

## Objective
Analyse 4 years of retail sales (2009-2012, 8,399 orders) and forecast the next 12 months.

## Tools
Python (pandas, statsmodels, matplotlib), Power BI, DAX

## Method
1. Cleaned data with pandas (checked nulls and duplicates) and aggregated to monthly sales.
2. Compared 4 models on a 6-month holdout: 12-month average, seasonal naive,
   Holt-Winters (trend + season), Holt-Winters (season only).
3. Selected seasonal Holt-Winters (MAPE 14.59%) for a 12-month forecast with an approximate range.
4. Built a 3-page Power BI dashboard with a star schema, DAX measures and slicers.

## Key findings
- Sales fell from 4.21M (2009) to 3.44M (2011), then rose 8.2% in 2012.
- Mild seasonality: higher in Dec/Jan, lower in mid-year.
- Furniture has the lowest profit margin of the three categories.
- Some sub-categories (e.g. Scissors, Rulers and Trimmers) lose money.

## Limitations
- Only 48 months of data, and monthly sales are noisy.
- A simple 12-month average (MAPE 13.07%) scored slightly better than Holt-Winters.
- No external factors (promotions, economy) are modelled.

## Screenshots
![Executive Summary](screenshots/1_executive_summary.png)
![Forecast](screenshots/2_forecast.png)
![Drill Down](screenshots/3_drill_down.png)
