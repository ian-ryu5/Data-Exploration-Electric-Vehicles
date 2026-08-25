# Electric Vehicle Population Data Exploration

A data exploration and modeling project analyzing Washington State's Electric Vehicle Population dataset — covering EV registrations, range characteristics by manufacturer, CAFV eligibility prediction, and registration growth trends.

## Overview

This project explores a public EV registration dataset to understand adoption patterns, range differences across manufacturers and vehicle types, and builds two predictive models: one classifying Clean Alternative Fuel Vehicle (CAFV) eligibility, and one projecting registration growth trends by make.

## Dataset

- **Source:** EV registration records (~112K rows), ~99.7% Washington State
- **Key fields:** Make, Model, Model Year, Electric Vehicle Type (BEV/PHEV), Electric Range, Base MSRP, County, CAFV Eligibility, Electric Utility

## What's Inside

- **Exploratory analysis** — distribution of electric range across the fleet, average range by make and vehicle type
- **CAFV eligibility model** — logistic regression predicting eligibility from Make, Model Year, Vehicle Type, and MSRP (deliberately excluding Electric Range, which directly defines eligibility) — achieves ~0.99 ROC AUC
- **Registration growth trend** — linear extrapolation of registration counts by top manufacturers over the last 10 complete years, framed explicitly as illustrative rather than predictive
- **Conclusion** — summary of findings, model results, and dataset limitations

## Files

| File | Description |
|---|---|
| `Ian_Ryu_Data_Exploration_Project_python.ipynb` | Full notebook (Python, pandas/scikit-learn/seaborn) |
| `Electric_Vehicle_Population_Data.csv` | Source dataset |
| `Ian_Ryu_Data_Exploration.pdf` | Read-only report version (code hidden, results only) |

## Requirements

```
pandas
matplotlib
seaborn
scikit-learn
```

## Limitations

- Geographic scope is almost entirely Washington State — findings may not generalize nationally
- Most recent model year in the data is a partial-year snapshot, not a complete year
- Growth projections use naive linear extrapolation and should be read as illustrative, not forecasts
