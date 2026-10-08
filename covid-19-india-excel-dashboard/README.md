# COVID-19 India — Excel Dashboard & Data Analysis

[![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)
[![Project Type](https://img.shields.io/badge/Project-Data%20Analysis-0F766E)]()
[![Scope](https://img.shields.io/badge/Scope-India%20State%2FUT%20Snapshot-2563EB)]()

An Excel-based COVID-19 data analysis project focused on an India state/UT snapshot. The workbook combines a structured source table, ratio calculations, state-level comparisons, zone summaries, and a dashboard for communicating the main results.

> **Data integrity note:** The workbook supplied for this portfolio is the source of truth. The repository documents what is actually present rather than inventing a dataset source, collection date, or business impact.

## Project Overview

The analysis answers questions such as:

- Which states/UTs have the highest and lowest recorded case counts?
- Which states have the highest and lowest discharge ratios?
- Which states have the highest and lowest death ratios?
- Where is the active-case ratio highest?
- How are total cases distributed across East, North, South, and West zones?

## Screenshot Gallery

This section is intentionally structured so you can publish screenshots from the real workbook.

Upload the images to the `screenshots/` folder using this naming pattern:

```text
screenshots/
├── 01-dashboard.png
├── 02-data-overview.png
├── 03-pivot-analysis.png
├── 04-summary-analysis.png
└── 05-workbook-overview.png
```

Then add the Markdown image links below:

```markdown
![Dashboard](screenshots/01-dashboard.png)
![Data Overview](screenshots/02-data-overview.png)
![Pivot Analysis](screenshots/03-pivot-analysis.png)
![Summary Analysis](screenshots/04-summary-analysis.png)
```

## Key Results From the Supplied Workbook

| KPI | Result |
|---|---:|
| States / UTs analyzed | 36 |
| Total recorded cases | 34,437,307 |
| Active cases | 135,918 |
| Discharged | 33,837,859 |
| Deaths | 463,530 |
| Overall discharge ratio | 98.26% |
| Overall death ratio | 1.35% |
| Overall active ratio | 0.39% |
| Total represented population | 1,429,869,880 |

The overall ratios above are recomputed from the state-level counts in the `Data` sheet. They are weighted by total recorded cases, not simple averages across states.

## Top Findings

**Case concentration.** Maharashtra has the highest recorded case count at **6,623,344**, followed by Kerala (**5,055,224**) and Karnataka (**2,991,614**).

**Discharge ratio.** Daman and Diu has the highest recorded discharge ratio (**99.96%**), while Mizoram has the lowest (**95.25%**).

**Death ratio.** Punjab has the highest recorded death ratio (**2.75%**), followed by Nagaland (**2.16%**) and Uttarakhand (**2.15%**).

**Active ratio.** Mizoram has the highest active ratio (**4.39%**), followed by Kerala (**1.37%**) and Ladakh (**0.73%**).

**Regional concentration.** The South zone has the highest total recorded cases at **13,650,538**, followed by West (**9,386,876**), East (**5,884,786**), and North (**5,515,107**).

## Data Quality & Validation

The supplied workbook has:

- **36 unique state/UT records**
- **12 columns**
- **0 missing cells** in the populated source table
- **0 duplicate state names**
- Exact case reconciliation: `Active + Discharged + Deaths = Total Cases`
- Ratio fields consistent with the count fields within normal rounding tolerance

See [`docs/QUALITY_AUDIT.md`](docs/QUALITY_AUDIT.md) for the detailed review.

## Important Data Caveats

This is a **snapshot-style dataset**, not a longitudinal time series: the source `Data` sheet contains no date column.

The workbook does not document an original external source URL or collection date. For that reason, this repository does not claim that the snapshot represents a specific day.

Two naming consistency issues were identified in the supplied workbook:

- `Telengana` appears in the source data; the standard spelling is `Telangana`.
- `Daman and Diu` is retained because it is present in the supplied workbook. The repository does not silently replace or reinterpret the supplied category.

The workbook also contains `Discharge Avg` and `Death Avg` as categorical labels (`Above Average` / `Below Average`). The corresponding `Recovered Index` and `Death Index` sheets use “Sum” wording for ratio fields; those totals are not meaningful overall averages and should not be presented as such.

## Workbook Structure

| Sheet | Purpose |
|---|---|
| `Data` | Source state/UT table and calculated ratios |
| `DashBoard` | Executive dashboard with highest/least comparisons |
| `Cases and Recovered` | State-wise total cases and discharged counts |
| `Active And Deaths` | State-wise active and death counts |
| `States and Zones` | Zone-level case summary |
| `Recovered Index` | State discharge-ratio ranking |
| `Death Index` | State death-ratio ranking |

## Repository Structure

```text
covid-19-india-excel-dashboard/
├── README.md
├── .gitignore
├── workbook/
│   ├── Covid Dashboard.xlsx
│   └── README.md
├── data/
│   └── covid_india_state_snapshot.csv
├── docs/
│   ├── DATA_DICTIONARY.md
│   ├── FINDINGS.md
│   ├── METHODOLOGY.md
│   └── QUALITY_AUDIT.md
└── screenshots/
    ├── 01-dashboard.png
    ├── 02-data-overview.png
    └── README.md
```

## How to Review the Project

1. Open `workbook/Covid Dashboard.xlsx` in Microsoft Excel.
2. Start on the `DashBoard` sheet.
3. Trace the headline metrics back to `Data`.
4. Review `Recovered Index` and `Death Index` for the state rankings.
5. Read `docs/FINDINGS.md` and `docs/QUALITY_AUDIT.md` for the analytical story and QA notes.

## Excel Skills Demonstrated

- Data organization and tabular analysis
- Ratio and percentage calculations
- Ranking and comparative analysis
- Conditional formatting
- Dashboard presentation
- State/zone aggregation
- Data-quality validation
- Analytical documentation and insight writing

## Recruiter View

This project is evidence of a complete Excel analytics workflow: understand the dataset, validate it, calculate metrics, compare segments, visualize results, and communicate the findings.

It should be evaluated on the analytical workflow and documentation rather than on unverifiable claims about external impact.

## Limitations

The analysis is descriptive. It does not establish causality, forecast future outcomes, measure public-health effectiveness, or assess the quality of the underlying external reporting.

Source attribution should be added if the original dataset source becomes available.
