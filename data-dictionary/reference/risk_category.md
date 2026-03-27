# Risk_Category

## Description
Defines customer risk categories used in collections prioritization.

## Grain
One row per risk category.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Risk_Category | Risk category code | Reference | System | | |
| Category_Range_Start | Credit score range start | Reference | System | | |
| Category_Range_End | Credit score range end | Reference | System | | |
| Active_Flag | Indicates active category | Reference | System | | |

## Keys
- **Primary Key**: Risk_Category
``
