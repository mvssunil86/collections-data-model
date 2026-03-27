# Dispute_Tracker

## Description
Tracks disputes raised against customer invoices during collections.

## Grain
One row per dispute.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Account_Num | Customer account number | Transaction | ERP | | |
| Invoice_Num | Invoice reference | Transaction | ERP | | |
| Dispute_Reason | Reason for dispute | Reference | | | |
| Dispute_Amount | Disputed amount | Transaction | | | |
| Dispute_Open_Dt | Dispute open date | Transaction | | | |
| Resolved_Dt | Dispute resolution date | Transaction | | | |
| Dispute_Status | Current status | Reference | | | |

## Keys
- **Primary Key**: Dispute_Key
- **Foreign Keys**:
  - Account_Key
  - Invoice_Key
  - Dispute_Reason
  - Dispute_Status
