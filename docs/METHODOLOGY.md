# Methodology

## 1. Data Understanding
The `Data` sheet was reviewed as the source table. It contains 415 expense records and 13 columns covering transaction identifiers, dates, organizational dimensions, amounts, approval status, budget fields, vendors, invoices, and month.

## 2. Data Quality Checks
The analysis validates: record count, Expense ID uniqueness, missing critical values, date coverage, allowed Approved values, budget relationships, and the arithmetic relationship `Amount + Budget Remaining = Budget Allocated`.

## 3. KPI Calculations
Key metrics are calculated from the supplied records:
- Total Expenses = sum of `Amount (INR)`
- Budget Allocated = sum of `Budget Allocated`
- Budget Remaining = sum of `Budget Remaining`
- Budget Utilization = `(Budget Allocated - Budget Remaining) / Budget Allocated`
- Approval Rate = approved records / total records

## 4. Aggregation
PivotTables summarize spending by department, category, month, payment method, approval status, and department budget comparison. These summaries feed the dashboard visuals.

## 5. Visualization
The Dashboard contains five visualizations: expense by department, expense by category, monthly trend, budget vs actual by department, and payment method.

## 6. Interpretation
Findings are descriptive and based only on the supplied portfolio dataset. They are presented as analytical observations rather than causal explanations.

## 7. QA Principle
No feature, metric, or business finding should be claimed unless it can be traced to the workbook or supporting calculations.
