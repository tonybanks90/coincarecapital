# Security & Compliance Guidelines

Coin Care Capital handles highly sensitive Personally Identifiable Information (PII), including National IDs, KRA PINs, and vehicle ownership documents. Adherence to strict security protocols is mandatory to comply with the **Kenyan Data Protection Act (2019)**.

## 1. Data Encryption

### Data in Transit
*   All API and web traffic MUST be routed over **HTTPS/TLS 1.3**.
*   No sensitive data (e.g., National ID) should ever be passed in a URL query string; it must be inside the body of a POST/PUT request.

### Data at Rest
*   The primary database (PostgreSQL) must utilize **AES-256 encryption at rest** (standard on AWS RDS, Supabase, and GCP Cloud SQL).
*   Sensitive columns (e.g., `national_id`, `kra_pin`) should be encrypted at the application layer before being written to the database using a robust KMS (Key Management Service).

## 2. Access Control (RBAC)

We employ Role-Based Access Control to ensure employees only see what they need to.

*   **Customer Role:** Can only view their own `user_id` data and linked loans via the Loan Tracker.
*   **Valuation Agent:** Can view vehicle details and upload photos, but CANNOT see the customer's payment history or change the interest rate.
*   **Loan Officer / Underwriter:** Can view credit history, approve loans, and generate final offer letters.
*   **Admin / Finance:** Can disburse funds, view ledger entries, and alter global settings.

## 3. Data Protection Act (Kenya) Compliance

*   **Consent:** The frontend application form MUST include a mandatory checkbox for data processing consent.
*   **Right to Erasure:** Customers who are rejected or have cleared their loans have the right to request data deletion. We must implement a "soft delete" or anonymization function that removes PII while retaining anonymized ledger data for accounting and CBK reporting.
*   **Data Residency:** Database servers should ideally be located in regions compliant with Kenyan data export laws (e.g., AWS af-south-1 in Cape Town or eu-west-1, pending legal review).

## 4. API Security

*   **Rate Limiting:** The `/auth/request-otp` endpoint must be strictly rate-limited (e.g., max 3 requests per 10 minutes per IP/Phone) to prevent SMS bombing attacks which cost the business money.
*   **CORS:** The backend API must only accept cross-origin requests from `coincarecapital.co.ke` and verified local development ports.
