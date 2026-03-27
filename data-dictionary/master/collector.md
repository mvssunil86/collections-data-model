# Collector

## Description
Stores details of collectors (collection agents), including role, contact details, team, and performance categorization.

## Grain
One row per collector.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Source_Collector_Id | Unique identifier for collector from source | Master | ERP | | |
| Collector_Name | Name of the collector | Master | ERP | | |
| Collector_Email_Id | Collector email address | Master | ERP | | |
| Collector_Role | Role (Agent, Supervisor, Lead) | Master | ERP | | |
| Collector_Team_Group | Team classification (Collection, Deduction, etc.) | Master | ERP | | |
| Supervisor_Id | Source identifier for supervisor | Master | ERP | | |
| Collector_Performance_Category | Performance bucket (A/B/C) | Master | ERP | | |
| Primary_Contact_Number | Primary phone number | Master | ERP | | |
| Alternate_Contact_Number | Alternate phone number | Master | ERP | | |

## Keys
- **Primary Key**: Collector_Key (Surrogate)
- **Natural Key**: Source_Collector_Id
- **Foreign Keys**: Supervisor_Id → Collector

## Notes
- Collector is managed as Slowly Changing Dimension (SCD Type 2).
