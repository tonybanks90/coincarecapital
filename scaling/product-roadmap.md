# Product Feature Roadmap

This document outlines the priority sequence for software features across the Coin Care Capital digital ecosystem (Web & Mobile).

---

## Phase 1: Immediate Priority

### 🔴 The Loan Tracker (Web App)
The most urgent feature request. Customers need a way to check the status of their loan application and track their repayment progress without calling the office.

*   **Goal:** Reduce customer support calls and provide transparency.
*   **Access:** A secure web page (`/track`) where users enter their Phone Number and an OTP (sent via SMS) or their Loan Reference Number.
*   **Features:**
    *   **Application Status:** Live progress bar (Submitted → Valuation Scheduled → NTSA Processing → Disbursed).
    *   **Active Loan Dashboard:** Current balance, next payment due date, and amount.
    *   **Payment History:** Ledger of past M-Pesa/Bank payments.
*   **Technical Requirement:** Requires the Phase 1 Backend API and Database to be deployed.

---

## Phase 2: Backend Automation

### 🟢 Custom CRM & Loan Processing Backend
Moving away from manually handling leads towards a fully automated pipeline.

*   **Goal:** Speed up internal processing time and eliminate paperwork.
*   **Features:**
    *   Internal dashboard for loan officers to approve/reject loans.
    *   Automated NTSA TIMS integration for instant logbook verification (if possible) or automated status flagging.
    *   Automated SMS dispatch for payment reminders and marketing blasts.

---

## Phase 3: The Mobile Experience

### 📱 Coin Care Mobile App (iOS & Android)
A dedicated React Native (Expo) app for returning customers.

*   **Goal:** Drive customer retention and make repeat borrowing frictionless.
*   **Features:**
    *   **Push Notifications:** Instant payment reminders and disbursement alerts.
    *   **In-App M-Pesa Payments:** Direct STK push integration so customers can pay directly inside the app.
    *   **One-Click Top-Up:** Let users request additional funds against their existing logbook equity instantly.

---

## Phase 4: AI & Operations Scaling

### 🤖 AI-Powered Automation
To handle increased loan volume without drastically increasing operational headcount.

*   **Goal:** Eliminate manual data entry and scale sales/collections via Artificial Intelligence.
*   **Features:**
    *   **AI Document Processing (OCR):** Automatically extract names, ID numbers, and vehicle registration numbers from uploaded IDs and logbook photos.
    *   **AI Voice Sales Agent:** A conversational bot to instantly call users who abandon their loan applications halfway through.
    *   **AI Collections Agent:** Automated, polite reminder calls for overdue payments.

---

## Phase 5: Field Agent Integration

### 🚗 Agent & Valuer Tools (Internal App)
A tool exclusively for Coin Care's field valuation officers and sales agents.

*   **Goal:** Standardize the valuation process and speed up final loan approvals from the field.
*   **Features:**
    *   GPS-tagged photo uploads of the vehicle (exterior, interior, engine).
    *   Digital inspection checklist.
    *   Instant upload to the internal CRM to automatically trigger the final loan offer to the customer.
