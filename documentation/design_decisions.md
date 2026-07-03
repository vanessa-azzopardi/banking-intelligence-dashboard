# Design Decisions

## Why use a star schema?

A star schema keeps the model clean, improves usability, and makes DAX calculations easier to maintain.

## Why use a dedicated date dimension?

The date dimension supports consistent filtering, month/year grouping and time-based calculations across multiple fact tables.

## Why use custom KPI cards?

The standard Power BI KPI visual assumes a target value. For macroeconomic indicators, comparison with the previous observation is more meaningful than comparison with an arbitrary target.

## Why include a refresh timestamp?

A refresh timestamp helps users understand how current the dashboard data is.

## Why use ECB data?

ECB data is public, reliable and directly relevant to banking, monetary policy and financial analysis.
