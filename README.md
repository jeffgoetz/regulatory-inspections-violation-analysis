# Regulatory Food Manufacturing Inspection Analysis

This project analyzes characteristics associated with reported violations in regulatory food manufacturing facility inspections conducted from 2022–2025. The analysis uses descriptive summaries, mixed-effects logistic regression, exploratory subgroup analysis, and year-over-year trend summaries to identify facility and inspection characteristics associated with reported violations.

## Overview

Regulatory inspections are an important component of food manufacturing oversight. This analysis examined whether risk level, region, square footage category, and establishment type were associated with reported inspection violations.

Because some facilities were inspected more than once, the primary model used a mixed-effects logistic regression approach with a random intercept for facility to account for repeated inspections within the same facility.

## Methods

The final analytic sample included 1,486 inspections from 817 unique facilities. The primary outcome was reported violation status, coded as a binary Yes/No variable.

The primary model included:

- Risk level
- Region
- Square footage category
- Facility-level random intercept

Exploratory analyses also examined:

- Violation rates by condensed establishment type within High- and Medium-risk facilities
- Year-over-year violation rates from 2022–2025
- Risk-stratified annual violation patterns

All analyses were conducted in R.

## Key Findings

Risk level was the strongest predictor of reported violations. Compared with Low-risk facilities, High-risk facilities had substantially higher adjusted odds of a reported violation, and Medium-risk facilities also had elevated odds.

Region and square footage category were also associated with violation status. In particular, Region 255 had higher adjusted odds of reported violations compared with the reference region.

Exploratory subgroup analysis suggested that violation rates were not uniform across establishment types. Fish/Seafood facilities stood out within the High-risk group, while Bottled Water and Baked Goods had higher observed violation rates within the Medium-risk group.

The year-over-year analysis showed that reported violation rates peaked in 2023, especially among High- and Medium-risk inspections. Descriptive review suggested that the 2023 increase may have been partially related to a larger share of High-risk Fish/Seafood inspections that year.

## Tools Used

- R
- dplyr
- janitor
- lme4
- ggplot2
- scales
- R Markdown

## Files

| Folder | Description |
|---|---|
| `code/` | R Markdown analysis code |
| `reports/` | Final analytic summary/report |
| `data/` | Data access note; original dataset not included |

## Data Availability

The original inspection-level dataset is not included in this repository because it contains internal administrative records. The code is provided to demonstrate the analytic workflow, modeling approach, and visualization process.

## Limitations

This analysis used observational administrative data, so findings should be interpreted as associations rather than causal effects. Some categories were sparse, limiting the stability of more detailed models. Establishment type analyses were exploratory and should be interpreted cautiously.

## Author

Jeff Goetz, MS  
Biostatistics | Public Health Analytics | Epidemiologic Data Analysis
