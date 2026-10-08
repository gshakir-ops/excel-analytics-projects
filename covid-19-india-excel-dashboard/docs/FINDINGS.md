# Findings

## Executive Summary

The supplied workbook contains **36 state/UT records** with **34,437,307 total recorded cases**. Of these, **135,918** are active, **33,837,859** are discharged, and **463,530** are deaths.

The underlying counts reconcile exactly:

`135,918 + 33,837,859 + 463,530 = 34,437,307`

## 1. Highest Recorded Case Counts

| Rank | State/UT | Total Cases |
|---:|---|---:|
| 1 | Maharashtra | 6,623,344 |
| 2 | Kerala | 5,055,224 |
| 3 | Karnataka | 2,991,614 |
| 4 | Tamil Nadu | 2,714,025 |
| 5 | Andhra Pradesh | 2,069,770 |

## 2. Discharge Ratio

Highest:

- Daman and Diu — **99.96%**
- Lakshadweep — **99.51%**
- Arunachal Pradesh — **99.42%**

Lowest:

- Mizoram — **95.25%**
- Punjab — **97.20%**
- Nagaland — **97.33%**

Overall weighted discharge ratio: **98.26%**.

## 3. Death Ratio

Highest:

- Punjab — **2.75%**
- Nagaland — **2.16%**
- Uttarakhand — **2.15%**

Lowest:

- Daman and Diu — **0.04%**
- Mizoram — **0.36%**
- Lakshadweep — **0.49%**

Overall weighted death ratio: **1.35%**.

## 4. Active Ratio

Highest:

- Mizoram — **4.39%**
- Kerala — **1.37%**
- Ladakh — **0.73%**

Overall weighted active ratio: **0.39%**.

## 5. Zone-Level Distribution

| Zone | Total Cases |
|---|---:|
| South | 13,650,538 |
| West | 9,386,876 |
| East | 5,884,786 |
| North | 5,515,107 |

South has the highest recorded case volume in the supplied dataset.

## Interpretation

The dataset shows differences across states in recorded case volume and outcome ratios. These should be treated as descriptive patterns in the supplied snapshot.

Because the workbook contains no date field and no documented source metadata, it is not appropriate to use this dataset for time-trend claims, current-status claims, or causal public-health conclusions.

## Portfolio Follow-Ups

1. Add the original source URL and dataset date.
2. Standardize state naming across all sheets.
3. Replace “sum of ratio” totals with weighted national rates where appropriate.
4. Add a dated source version to enable time-series analysis.
