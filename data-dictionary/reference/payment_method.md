# Payment_Method

## Description
Defines supported payment methods for customer payments.

## Grain
One row per payment method.

## Columns

| Column Name | Description | Type | Source System | Source Table | Source Column |
|------------|------------|------|---------------|--------------|---------------|
| Payment_Method | Payment method name | Reference | ERP | | |
| Is_Secure_Flag | Indicates secure payment method | Reference | System | | |
| Active_Flag | Indicates active payment method | Reference | System | | |

## Keys
- **Primary Key**: Payment_Method

