# Data Dictionary

| Column | Type | Description | Analytical Use |
|---|---|---|---|
| Expense ID | Text | Unique expense identifier in the form EXP-XXXX | Record tracking and uniqueness QA |
| Date | Date | Transaction date during 2025 | Time-series analysis |
| Department | Text | Department associated with the expense | Department spend comparison |
| Category | Text | Expense category | Category mix and concentration |
| Description | Text | Text description of the expense | Context / qualitative review |
| Amount (INR) | Numeric | Recorded expense amount in INR | Primary spend KPI |
| Payment Method | Text | Method used to pay the expense | Payment-method mix |
| Approved | Text | Whether the expense is marked Yes or No | Approval-rate analysis |
| Budget Allocated | Numeric | Budget associated with the record | Budget analysis |
| Budget Remaining | Numeric | Remaining budget associated with the record | Budget utilization |
| Vendor Name | Text | Vendor associated with the expense | Vendor concentration |
| Invoice Number | Text | Invoice identifier | Transaction traceability |
| Month | Text | Three-letter month derived from Date | Monthly summaries and charts |

## Derived Field
`Month` is calculated from `Date` using the structured formula pattern `=TEXT(tblExpenses[[#This Row],[Date]],"mmm")`.

## Dataset Scope
- Records: 415
- Date coverage: January–December 2025
- Departments: 6
- Categories: 8
- Vendors: 10
- Payment methods: 4
