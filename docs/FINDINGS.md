# Findings & Business Interpretation

## Executive Summary
The dataset contains 415 expense transactions recorded across 2025. Total recorded spending is **INR 18,405,183** against **INR 22,953,950** of represented budget, leaving **INR 4,548,767** and producing an overall budget utilization of **80.18%**.

## 1. Spending Concentration
**Consulting** is the largest category at **INR 6,030,171**, representing **32.76%** of total spend. Equipment and Marketing follow at INR 3,671,418 and INR 3,505,155. Together, Consulting, Equipment, and Marketing account for **71.75%** of total spending.

**Interpretation:** A large proportion of spending is concentrated in three categories. In a real operating environment, these categories would be natural candidates for deeper variance, vendor, and policy analysis.

## 2. Department Spending
Department-level spend ranges from **INR 2,453,972** in Sales to **INR 3,616,924** in HR. HR represents **19.65%** of total spend, followed by Engineering at 18.29% and Operations at 18.18%.

**Interpretation:** Spend is distributed across all six departments rather than being dominated by a single department.

## 3. Monthly Trend
**July** has the highest monthly spend at **INR 2,119,404 (11.52%)**, while **February** has the lowest at **INR 1,058,599 (5.75%)**.

**Interpretation:** The monthly series shows noticeable variation across the year. The dataset alone does not explain the reasons for the July peak, so causal explanations should not be inferred without additional operational information.

## 4. Budget Utilization
The dataset records **INR 18,405,183** of spend against **INR 22,953,950** allocated, with **INR 4,548,767** remaining.

**Interpretation:** Overall utilization is **80.18%**. Department-level budget comparisons in the workbook provide a basis for investigating where spending is closer to or farther from allocated budgets.

## 5. Approval Status
There are **338 approved** and **77 not-approved** records, giving an approval rate of **81.45%**.

**Interpretation:** The workbook distinguishes approval status clearly, but the dataset does not provide reasons for non-approval. Therefore, the analysis should not assume that a non-approved record is erroneous or problematic.

## 6. Vendor Concentration
**PowerGrid Co** has the highest recorded vendor spend at **INR 2,597,554 (14.11%)**. The remaining vendor spend is distributed across nine other vendors.

**Interpretation:** Vendor-level concentration can be used as a starting point for procurement or supplier-spend review, subject to real business context.

## 7. Payment Method
**Cheque** is the largest payment method by spend at **INR 5,477,461 (29.76%)**, followed by Bank Transfer at 26.67%, Cash at 23.85%, and Credit Card at 19.72%.

**Interpretation:** Payment-method mix is relatively distributed, with cheque representing the largest share. A real organization could combine this view with payment policy and transaction-processing cost data for further analysis.

## Recommended Analytical Follow-ups
1. Investigate the drivers of the July spending peak using transaction-level detail.
2. Examine Consulting, Equipment, and Marketing spend by vendor and department.
3. Compare department-level actual spend against allocated budgets to identify larger variances.
4. Review non-approved transactions to understand the reasons and potential process patterns.
5. Combine vendor and category analysis to identify major supplier relationships.

## Limitations
These are descriptive findings from a portfolio dataset. They should not be interpreted as evidence of financial performance, policy compliance, cost savings opportunities, or operational problems without additional business context.
