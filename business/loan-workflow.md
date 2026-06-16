# Core Business Workflow: Logbook Loans

This document outlines the standard operating procedure and state machine for a Logbook Loan application at Coin Care Capital.

## Application Lifecycle Flowchart

The following Mermaid flowchart details the customer journey from the initial application on the web/mobile platform to final disbursement and repayment.

```mermaid
graph TD
    %% Define styles
    classDef customer fill:#e0f2fe,stroke:#0369a1,stroke-width:2px;
    classDef system fill:#f0fdf4,stroke:#15803d,stroke-width:2px;
    classDef agent fill:#fef08a,stroke:#a16207,stroke-width:2px;
    classDef external fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,stroke-dasharray: 5 5;

    %% Nodes
    Start((Start)) --> App[Customer Submits Application]:::customer
    App --> CRM[Lead enters CRM/Sanity]:::system
    CRM --> Call[Loan Officer Calls Customer]:::agent
    
    Call --> |Qualifies| Doc[Document Verification]:::agent
    Call --> |Disqualifies| Reject[Reject Lead]:::system
    
    Doc --> Val[Vehicle Valuation Scheduled]:::agent
    Val --> |Valuation Complete| Offer[Loan Offer Generated]:::system
    Offer --> Accept{Customer Accepts?}:::customer
    
    Accept -->|Yes| NTSA[Joint Registration via eCitizen]:::external
    Accept -->|No| Cancel[Cancel Application]:::system
    
    NTSA --> |Success| Disburse[Funds Disbursed to Bank/M-Pesa]:::system
    Disburse --> Repay[Monthly Repayment Cycle Begins]:::customer
    Repay --> |Loan Cleared| Transfer[Transfer Logbook back to Customer]:::external
    Transfer --> End((End))

```

## Key SLAs (Service Level Agreements)
*   **Initial Call:** Within 15 minutes of web application submission.
*   **Valuation:** Within 1 hour (Nairobi Metro area).
*   **Disbursement:** Under 24 hours from initial application (provided NTSA systems are online).
