# Quality Audit

## Scope

This QA review is based on the supplied `Covid Dashboard.xlsx` workbook and its populated `Data` sheet.

## Structural Checks

| Check | Result |
|---|---:|
| Records | 36 |
| Columns | 12 |
| Unique state/UT names | 36 |
| Missing populated-table cells | 0 |
| Duplicate state/UT names | 0 |
| Distinct zones | 4 |

## Reconciliation

The following relationship holds exactly across the supplied records:

`Active + Discharged + Deaths = Total Cases`

Total cases: **34,437,307**

Active + discharged + deaths: **34,437,307**

## Recomputed Ratios

| Ratio | Workbook concept | Maximum absolute difference |
|---|---|---:|
| Active Ratio | Active / Total Cases × 100 | 0.00494 percentage points |
| Discharge Ratio | Discharged / Total Cases × 100 | 0.00491 percentage points |
| Death Ratio | Deaths / Total Cases × 100 | 0.00500 percentage points |

The differences are consistent with two-decimal display rounding.

## Overall Weighted Ratios

| Metric | Recomputed result |
|---|---:|
| Active ratio | 0.39% |
| Discharge ratio | 98.26% |
| Death ratio | 1.35% |

These are calculated from the national totals in the supplied table.

## Issues Identified for Portfolio Polish

### 1. Missing provenance

The workbook does not contain a source URL or collection date. This is the biggest documentation gap because a recruiter cannot independently trace the dataset.

**Recommendation:** add the original source, retrieval date, and licensing/usage note once known.

### 2. “Grand Total” in ratio index sheets

`Recovered Index` and `Death Index` use “Sum of ... Ratio” and a grand total. Summing percentages across states does not provide an interpretable national rate.

**Recommendation:** label the overall KPI using a weighted ratio calculated from total counts, or explicitly label the table as state-level ranking only.

### 3. Naming consistency

The supplied data uses `Telengana`. The standard spelling is `Telangana`.

The dashboard also shows `MP` in one place while the source table uses `Madhya Pradesh`.

**Recommendation:** standardize names across all sheets and dashboard outputs.

### 4. Historical scope needs to be documented

The presence of `Daman and Diu` suggests the workbook reflects a historical state/UT classification rather than today's administrative structure. The source table itself does not document the snapshot date.

**Recommendation:** add the original dataset date/source metadata before calling the dataset “current” or assigning it to a specific period.

## QA Conclusion

The core count fields are internally consistent, and the displayed ratio fields are mathematically consistent with the underlying counts within rounding tolerance. The main improvements are provenance, historical scope documentation, and presentation consistency rather than fundamental arithmetic correction.
