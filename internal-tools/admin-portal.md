# Internal Admin & Loan Management Portal

While the public website handles customer acquisition, the **Internal Admin Portal** is the secure, centralized hub where your staff manages the entire business.

This portal replaces scattered spreadsheets, disconnected emails, and manual tracking systems, providing a single source of truth for operations.

## 1. Internal Loan Tracking Dashboard

At the core of the portal is a comprehensive view of all loans across their lifecycle.

*   **The Kanban Board:** A visual pipeline where loans move through stages: `New Lead` ➔ `Valuation Pending` ➔ `Underwriting` ➔ `NTSA Processing` ➔ `Funded`.
*   **360-Degree Customer Profile:** Clicking on a loan reveals everything in one place:
    *   Uploaded documents (ID, Logbook photos).
    *   AI-extracted data (Chassis numbers, Engine numbers).
    *   Communication history (SMS logs, AI call transcripts).
*   **Repayment Ledger:** An automated view of expected vs. received payments, flagging accounts that are in arrears.

## 2. User Management & Access Control

Security is paramount when handling financial data. The portal includes strict Role-Based Access Control (RBAC) so employees only see what they need to see.

*   **Super Admin (Founders/Directors):** Full access to financial metrics, ledger adjustments, and employee permissions.
*   **Underwriters / Loan Officers:** Can view credit histories, approve loans, and generate final offer letters. Cannot delete records.
*   **Field Valuers:** Mobile-optimized access. Can only see the vehicle details and location they are assigned to inspect. Can upload photos and enter the final valuation amount.
*   **Customer Support:** Can view loan status and chat history to assist calling customers, but cannot view the internal valuation logic or adjust interest rates.

## 3. Automated Reporting & Analytics

The portal removes the need for manual end-of-month reporting.

*   **Disbursement Velocity:** Tracks how fast loans are processed (e.g., "Average time from application to funding: 18 hours").
*   **Portfolio Health:** Live charts showing the percentage of the loan book in good standing versus 30, 60, or 90 days in arrears.
*   **Agent Performance:** Metrics on how many loans each officer closed or how many valuations a field agent completed in a week.

## 4. Integration Hub

The portal acts as the command center where all third-party tools connect:
*   **SMS Gateways** for bulk messaging.
*   **AI Voice Agents** for managing automated call campaigns.
*   **Payment Gateways** (M-Pesa Paybill APIs) for automatic reconciliation of incoming payments.
