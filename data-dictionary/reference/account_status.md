# Account_Status

## Description
Defines the status of a customer account used for credit and collections control.

## Grain
One row per account status code.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Account_Status | Account status code | Reference | ERP | | |
| Account_Status_Description | Description of account status | Reference | ERP | | |
| Active_Flag | Indicates active status | Reference | System | | |
| Effective_Start_Dt | Status effective start date | Reference | System | | |
| Effective_End_Dt | Status effective end date | Reference | System | | |

## Keys
- **Primary Key**: Account_Status
``
