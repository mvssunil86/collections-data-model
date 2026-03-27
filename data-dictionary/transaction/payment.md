# Payment

## Description
Stores customer payment transactions.

## Grain
One row per payment transaction.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Payment_Id | Payment receipt identifier | Transaction | ERP | | |
| Account_Num | Customer account number | Transaction | ERP | | |
| Invoice_Num | Invoice number | Transaction | ERP | | |
| Payment_Amount | Amount paid | Transaction | ERP | | |
| Payment_Dt | Payment date | Transaction | ERP | | |
| Payment_Method | Payment method used | Reference | | | |
| Payment_Status | Success/Failure | Reference | | | |
| Failure_Reason | Failure reason if any | Transaction | | | |

## Keys
- **Primary Key**: Payment_Key
- **Natural Key**: Payment_Id
- **Foreign Keys**:
  - Account_Key
  - Invoice_Key
  - Payment_Method
