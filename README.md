# Electricity Consumption Insight — Synthetic Practice Dataset

This folder contains five synthetic CSV datasets (1,000 base records each) for a data-science skill assessment.

## Files
- `meter_readings.csv`: timestamp, customer_id, consumption_kwh (includes intentionally injected missing values, duplicate rows, negative values and a few outliers).
- `customers.csv`: customer_id, segment, area, connection_type (includes inconsistent segment labels).
- `weather.csv`: timestamp, temperature_c, humidity_pct, rain_mm (includes weather gaps and duplicate rows).
- `calendar.csv`: timestamp, weekday, holiday, season.
- `tariff.csv`: timestamp, tariff_category, peak_period.
- `master_dataset_clean.csv`: a convenience joined dataset based on the base data for quick exploration. For the assessment, demonstrate your own cleaning and merging from the five raw CSVs.

## Important
All data are synthetic and for learning/demo use only. They do not represent a real utility or real customer records. Each of the five raw CSV files contains exactly 1,000 rows. Duplicate records are embedded within the 1,000 rows to demonstrate duplicate removal.

## Suggested target
Predict `consumption_kwh` as a regression task.

## Suggested workflow
1. Load all CSVs with pandas.
2. Inspect shape, dtypes, missing values, duplicates and value ranges.
3. Normalize `segment`, remove duplicate rows, treat negative consumption as invalid, impute missing values, and investigate outliers.
4. Merge meter readings with customer metadata by `customer_id`, and weather/calendar/tariff by timestamp.
5. Engineer `hour`, `day_of_week`, `is_weekend`, `month`, and encode categorical columns.
6. Use a time-based train/test split for regression.
7. Train a baseline and one chosen model; report MAE, RMSE and R² from actual predictions.
8. Plot hourly demand, consumption by segment, temperature vs consumption, weekend vs weekday, and tariff-period demand.
9. Export cleaned data, notebook, Excel workbook, and a short insight presentation.
