# Credit_Rating

## Description
Stores external credit rating classifications and score ranges.

## Grain
One row per credit rating.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Credit_Rating | Credit rating code | Reference | External | | |
| Credit_Score_Range | Score range associated | Reference | External | | |
| Active_Flag | Indicates active rating | Reference | System | | |

## Keys
- **Primary Key**: Credit_Rating
``
