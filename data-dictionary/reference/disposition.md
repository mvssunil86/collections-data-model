# Disposition

## Description
Defines interaction outcomes recorded during collections activity.

## Grain
One row per disposition and sub‑disposition combination.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Disposition_Code | Primary disposition code | Reference | System | | |
| Disposition_Description | Disposition description | Reference | System | | |
| Sub_Disposition_Code | Sub‑disposition code | Reference | System | | |
| Sub_Disposition_Description | Sub‑disposition description | Reference | System | | |
| Active_Flag | Indicates active disposition | Reference | System | | |

## Keys
- **Primary Key**: Disposition_Code, Sub_Disposition_Code
