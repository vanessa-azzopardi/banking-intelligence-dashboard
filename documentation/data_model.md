# Data Model

The dashboard uses a star schema model.

## Dimension Table

### Dim_Date

Contains date-related fields used for filtering and time intelligence.

Examples:

- Date
- Year
- Quarter
- Month
- Month Year
- Month Short Name
- Start of Month
- End of Month
- Is Current Year
- Is Current Month

## Fact Tables

### Fact_ExchangeRates

Contains EUR/USD exchange rate data.

### Fact_DepositRates

Contains ECB deposit facility rate data.

### Fact_InflationRates

Contains euro area inflation data.

### Fact_LendingRates

Contains euro area lending rate data.

## Measures Table

### Measures

Stores all DAX measures used in the report.

## Metadata Table

Stores dashboard metadata, including the last refresh timestamp.
