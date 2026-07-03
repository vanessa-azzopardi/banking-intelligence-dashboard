# DAX Measures

This project uses DAX measures to calculate current values, previous values, absolute changes, percentage changes and KPI indicators.

## Example: Current Exchange Rate

```DAX
Current Exchange Rate =
LASTNONBLANKVALUE(
    Dim_Date[Date],
    AVERAGE(Fact_ExchangeRates[Exchange Rate])
)
```

## Example: Previous Exchange Rate

```DAX
Previous Exchange Rate =
VAR CurrentDate =
    MAX(Fact_ExchangeRates[Date])
VAR PreviousDate =
    CALCULATE(
        MAX(Fact_ExchangeRates[Date]),
        FILTER(
            ALL(Fact_ExchangeRates),
            Fact_ExchangeRates[Date] < CurrentDate
        )
    )
RETURN
    CALCULATE(
        [Average Exchange Rate],
        Fact_ExchangeRates[Date] = PreviousDate
    )
```

## Example: Exchange Rate % Change

```DAX
Exchange Rate % Change =
DIVIDE(
    [Exchange Rate Change],
    [Previous Exchange Rate]
)
```

## Example: Last Refresh Display

```DAX
Last Refresh Display =
"Last refreshed (UTC): "
&
FORMAT(
    MAX(Metadata[Value]),
    "dd MMM yyyy HH:mm"
)
```
