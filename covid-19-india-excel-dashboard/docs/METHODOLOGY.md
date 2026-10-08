# Methodology

## 1. Source Review

The supplied Excel workbook was reviewed sheet-by-sheet, with the `Data` sheet treated as the source table for numerical validation.

## 2. Data Validation

The following checks were performed:

- populated row and column count
- missing-cell check
- duplicate state/UT check
- zone category check
- count reconciliation
- ratio recomputation from base counts

## 3. KPI Construction

Overall metrics are recomputed from the underlying state/UT counts rather than using sums of percentage fields.

For example:

`Overall discharge ratio = SUM(Discharged) / SUM(Total Cases) × 100`

This is preferable to summing state-level percentages.

## 4. Comparative Analysis

State rankings use:

- Total Cases
- Discharge Ratio
- Death Ratio
- Active Ratio

Zone totals are calculated by summing Total Cases within each zone.

## 5. Interpretation Rules

The analysis is descriptive. Observations are presented as patterns in the supplied records, not as causal explanations.

No external claims, public-health conclusions, or business impact claims are made without evidence in the workbook or a documented external source.

## 6. Reproducibility

The CSV in `data/` is a direct tabular export of the populated `Data` sheet. The original Excel workbook is preserved in the portfolio package so a reviewer can compare the repository analysis with the actual workbook.
