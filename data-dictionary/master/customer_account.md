# Customer_Account

## Description
Stores customer account, credit, risk, billing, and accounts payable contact information used in collections.

## Grain
One row per customer account.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Account_Num | Customer account number | Master | ERP | | |
| Account_Name | Customer name | Master | ERP | | |
| Account_Activation_Dt | Account activation date | Master | ERP | | |
| Account_Tenure | Account age/tenure | Derived | Calculated | | |
| Business_Unit | Business unit mapping | Master | ERP | | |
| Region | Region | Master | ERP | | |
| Parent_Group | Parent account/group | Master | ERP | | |
| Credit_Limit | Credit limit | Master | ERP | | |
| Credit_Score | Credit score | Master | External | | |
| Account_Status | Account status | Reference | | | |
| Billing_Currency | Billing currency | Reference | | | |
| Payment_Term | Default payment term | Reference | | | |
| Payment_Method | Default payment method | Reference | | | |
| Credit_Rating | External credit rating | Reference | | | |
| Risk_Category | Risk category | Reference | | | |
| Dispute_Flag | Indicates open disputes | Derived | | | |

## Keys
- **Primary Key**: Account_Key (Surrogate)
- **Natural Key**: Account_Num
- **Foreign Keys**:
  - Credit_Rating
  - Risk_Category
  - Account_Status
  - Payment_Term
  - Payment_Method
  - Billing_Currency

## Notes
- Derived metrics are maintained in account-level summary tables.
