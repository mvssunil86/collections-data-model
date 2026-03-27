# Collection_Status

## Description
Defines lifecycle statuses of invoices during the collection process.

## Grain
One row per collection status.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Collection_Status | Collection status code | Reference | System | | |
| Collection_Status_Description | Status description | Reference | System | | |
| Active_Flag | Indicates active status | Reference | System | | |

## Keys
- **Primary Key**: Collection_Status
``
