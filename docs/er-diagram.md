# Collections Data Model – ER Diagram

```mermaid
erDiagram

    COLLECTOR ||--o{ CUSTOMER_ACCOUNT : assigns
    CUSTOMER_ACCOUNT ||--o{ INVOICE : has
    CUSTOMER_ACCOUNT ||--o{ PAYMENT : makes
    CUSTOMER_ACCOUNT ||--o{ DISPUTE_TRACKER : raises

    INVOICE ||--o{ PAYMENT : settles
    INVOICE ||--o{ DISPUTE_TRACKER : disputed_for

    CUSTOMER_ACCOUNT }o--|| ACCOUNT_STATUS : has
    CUSTOMER_ACCOUNT }o--|| CREDIT_RATING : has
    CUSTOMER_ACCOUNT }o--|| RISK_CATEGORY : has
    CUSTOMER_ACCOUNT }o--|| PAYMENT_TERMS : uses
    CUSTOMER_ACCOUNT }o--|| PAYMENT_METHOD : defaults_to
    CUSTOMER_ACCOUNT }o--|| CURRENCY : billed_in

    INVOICE }o--|| COLLECTION_STATUS : tracked_by
    INVOICE }o--|| AGING_BUCKET : aged_into
    INVOICE }o--|| PAYMENT_TERMS : uses
    INVOICE }o--|| PAYMENT_METHOD : uses
    INVOICE }o--|| CURRENCY : billed_in
    INVOICE }o--|| DISPOSITION : classified_by

    PAYMENT }o--|| PAYMENT_METHOD : paid_via
    DISPUTE_TRACKER }o--|| DISPUTE_REASON : categorized_by

    COLLECTOR {
        string Source_Collector_Id PK
        string Collector_Name
        string Collector_Role
        string Collector_Team_Group
        string Supervisor_Id FK
    }

    CUSTOMER_ACCOUNT {
        string Account_Num PK
        string Account_Name
        string Region
        decimal Credit_Limit
        string Account_Status FK
        string Credit_Rating FK
        string Risk_Category FK
    }

    INVOICE {
        string Invoice_Num PK
        string Account_Num FK
        date Invoice_Dt
        date Invoice_Due_Dt
        decimal Invoice_Amount
        decimal Outstanding_Amount
    }

    PAYMENT {
        string Payment_Id PK
        string Account_Num FK
        string Invoice_Num FK
        decimal Payment_Amount
        date Payment_Dt
    }

    DISPUTE_TRACKER {
        string Dispute_Id PK
        string Account_Num FK
        string Invoice_Num FK
        decimal Dispute_Amount
        string Dispute_Status
    }
``
