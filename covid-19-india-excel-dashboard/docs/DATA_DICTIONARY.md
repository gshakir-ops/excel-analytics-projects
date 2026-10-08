# Data Dictionary

| Column | Type | Description | Analytical Role |
|---|---|---|---|
| State/UTs | Text | State or union territory label | Geographic comparison |
| Zone | Text | Broad regional grouping: East, North, South, West | Regional aggregation |
| Total Cases | Integer | Recorded COVID-19 cases for the state/UT snapshot | Primary volume KPI |
| Active | Integer | Recorded active cases | Snapshot-load indicator |
| Discharged | Integer | Recorded discharged/recovered cases | Recovery comparison |
| Deaths | Integer | Recorded deaths | Mortality comparison |
| Active Ratio | Percentage | Active cases as a percentage of total cases | State comparison |
| Discharge Ratio | Percentage | Discharged cases as a percentage of total cases | Recovery-rate comparison |
| Discharge Avg | Category | Above/Below average classification of discharge ratio | Relative classification |
| Death Ratio | Percentage | Deaths as a percentage of total cases | Mortality comparison |
| Death Avg | Category | Above/Below average classification of death ratio | Relative classification |
| Population | Integer | Population value supplied for the state/UT | Population context |

## Derived Metrics Used in the QA Review

**Active ratio**

`Active / Total Cases × 100`

**Discharge ratio**

`Discharged / Total Cases × 100`

**Death ratio**

`Deaths / Total Cases × 100`

## Dataset Scope

- 36 state/UT rows
- 4 zones
- 12 columns
- Snapshot-style data; no date field in the source table
