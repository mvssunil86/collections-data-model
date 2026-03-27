# Invoice

## Description
Stores invoice-level billing and collection attributes.

## Grain
One row per invoice.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Invoice_Num | Invoice/document number | Transaction | ERP | | |
| Account_Num | Customer account number | Transaction | ERP | | |
| Invoice_Amount | Invoice amount | Transaction | ERP | | |
| Invoice_Dt | Invoice date | Transaction | ERP | | |
| Invoice_Due_Dt | Due date | Transaction | ERP | | |
| Outstanding_Amount | Remaining balance | Transaction | ERP | | |
| Days_Past_Due | Days past due | Derived | | | |
| Disposition | Disposition from interaction | Reference | | | |
| Promise_To_Pay_Amount | PTP amount | Transaction | | | |
| Promise_To_Pay_Dt | PTP date | Transaction | | | |

## Keys
- **Primary Key**: Invoice_Key
- **Natural Key**: Invoice_Num
- **Foreign Keys**:
  - Account_Key
  - Payment_Term
  - Payment_Method
  - Currency

## Notes
- Supports partial payments and dispute tracking.
