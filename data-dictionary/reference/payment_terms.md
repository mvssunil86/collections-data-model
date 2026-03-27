# Payment_Terms

## Description
Defines payment terms applied at account or invoice level.

## Grain
One row per payment term.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Payment_Term_Code | Payment term code | Reference | ERP | | |
| Payment_Term_Description | Payment term description | Reference | ERP | | |
| Installment_Plan_Flag | Indicates installment plan | Reference | System | | |
| Active_Flag | Indicates active payment term | Reference | System | | |

## Keys
- **Primary Key**: Payment_Term_Code
``
