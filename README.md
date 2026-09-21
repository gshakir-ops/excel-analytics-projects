# Expense Analytics Dashboard — Excel Data Analysis Project

## Project Overview
This project analyzes a 2025 expense dataset containing **415 transactions** across six departments. The workbook combines structured Excel data, data-quality checks, PivotTable analysis, dashboard visualizations, and business-focused findings.

The purpose is to demonstrate an end-to-end Excel analytics workflow: understand the dataset, validate its quality, summarize performance, visualize patterns, and communicate findings clearly.

> **Data note:** The dataset is used as a portfolio/business-analysis dataset. The findings describe the supplied records and are not claims about a real company.

## Business Questions
- How much was spent during 2025?
- How is spending distributed across departments and categories?
- How does spending change month to month?
- How much of the represented budget has been used?
- What is the approval rate?
- Which vendors and payment methods account for the most spending?

## Key Results
| KPI | Result |
|---|---:|
| Total expenses | INR 18,405,183 |
| Budget allocated | INR 22,953,950 |
| Budget remaining | INR 4,548,767 |
| Budget utilization | 80.18% |
| Transactions | 415 |
| Approval rate | 81.45% (338/415) |
| Departments | 6 |
| Categories | 8 |
| Vendors | 10 |

## Key Findings
1. **Consulting is the largest expense category**, at INR 6,030,171 (32.76% of total spending).
2. **HR has the highest department-level spend**, at INR 3,616,924 (19.65%).
3. **July is the highest-spend month**, at INR 2,119,404 (11.52%).
4. **PowerGrid Co has the highest vendor spend**, at INR 2,597,554 (14.11%).
5. **Cheque is the largest payment method by spend**, at INR 5,477,461 (29.76%).
6. **Consulting, Equipment, and Marketing together represent 71.75% of total spend**, indicating concentration in three categories.

## Data Quality
The enhanced workbook includes a dedicated **Data Quality** sheet. Checks cover record count, ID uniqueness, missing values, date range, allowed approval values, budget relationships, and budget arithmetic. All checks documented there pass for the supplied 415 records.

## Workbook Structure
- **Dashboard** — KPI presentation and five visualizations
- **Data** — 415-record structured expense table
- **Pivot** — PivotTable-based summaries supporting the dashboard
- **Data Quality** — documented validation checks
- **Insights** — evidence-based findings and interpretation
- **Chart1 / Chart2 / Chart3** — supporting chart sheets

The source workbook contains **seven PivotTables**, dashboard charts, slicer components, and a macro-enabled VBA project. VBA code/functionality has not been independently executed as part of this portfolio QA, so the project does not rely on unverified automation claims.

## Excel Techniques Demonstrated
- Excel Tables and structured references
- PivotTables and Pivot-based summaries
- Dashboard charting
- Slicer components
- Formula-driven Month field
- Data validation / quality checks
- KPI calculation
- Business-focused insight writing

## Repository Structure
```text
excel-analytics-projects/
├── README.md
├── workbook/
│   └── expense_analysis_dashboard_enhanced.xlsm
├── data/
│   └── expense_dataset.csv
├── docs/
│   ├── DATA_DICTIONARY.md
│   ├── METHODOLOGY.md
│   └── FINDINGS.md
└── screenshots/
    ├── README.md
    └── 01-dashboard.png
```

## How to Review
1. Open the workbook in Microsoft Excel.
2. Start with the **Dashboard** sheet.
3. Use the **Data Quality** and **Insights** sheets to understand validation and findings.
4. Open the **Pivot** sheet to inspect the supporting summaries.
5. Review `docs/FINDINGS.md` for the written analytical story.

## Limitations
This analysis is descriptive. It does not establish causality, forecast future spending, or assess whether individual expenses were appropriate. Business recommendations should be validated against the organization’s policies, targets, and operational context before being acted upon.
