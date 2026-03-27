# Dispute_Reason

## Description
Defines standardized reasons for disputes raised during collections.

## Grain
One row per dispute reason.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Reason_Code | Dispute reason code | Reference | System | | |
| Reason_Name | Dispute reason description | Reference | System | | |
| Active_Flag | Indicates active reason | Reference | System | | |

## Keys
- **Primary Key**: Reason_Code
``
