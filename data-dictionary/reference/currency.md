# Currency

## Description
Defines ISO currency codes used in billing and payments.

## Grain
One row per currency code.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| ISO_Currency_Code | ISO 4217 currency code | Reference | ERP | | |
| Currency_Description | Currency description | Reference | ERP | | |
| Active_Flag | Indicates active currency | Reference | System | | |

## Keys
- **Primary Key**: ISO_Currency_Code
