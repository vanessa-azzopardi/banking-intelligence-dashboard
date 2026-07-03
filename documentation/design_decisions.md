# Design Decisions

## Schema

A star schema was used to keep the model clean, improve usability, and makes DAX calculations easier to maintain.

## A dedicated date dimension

A dedicated date dimension wsa created to support consistent filtering, month/year grouping and time-based calculations across multiple fact tables.

## Use of custom KPI cards

The standard Power BI KPI visual assumes a target value. For macroeconomic indicators, comparison with the previous observation was deemed more meaningful than comparison with an arbitrary target, hence custom KPI cards were used to enable comparisons with previous observations, such as prior month.

## A refresh timestamp

A refresh timestamp was included to indicate to the users how recent the dashboard data is.

## Use of ECB data

ECB data is public, reliable and directly relevant to banking, monetary policy and financial analysis.  It is also updated on daily basis and therefore a suitable data source to showcase automated, periodic data monitoring.
