# Product Feature Roadmap

This document outlines the priority sequence for software features across the Coin Care Capital digital ecosystem (Web & Mobile).

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

## Phase 2: Backend Automation

### 🟢 Custom CRM & Loan Processing Backend
Moving away from manually handling leads towards a fully automated pipeline.

*   **Goal:** Speed up internal processing time.
*   **Features:**
    *   Internal dashboard for loan officers.
    *   Automated NTSA TIMS integration for instant logbook verification (if possible) or automated status flagging.
    *   Automated SMS dispatch for payment reminders.

## Phase 3: The Mobile Experience

### 📱 Coin Care Mobile App (iOS & Android)
A dedicated React Native (Expo) app for returning customers.

*   **Goal:** Drive customer retention and make repeat borrowing frictionless.
*   **Features:**
    *   **Push Notifications:** Instant payment reminders and disbursement alerts.
    *   **In-App M-Pesa Payments:** Direct STK push integration.
    *   **One-Click Top-Up:** Let users request additional funds against their existing logbook equity.

## Phase 4: Agent & Valuer Tools

### 🚗 Valuer Mobile App (Internal)
A tool exclusively for Coin Care's field valuation officers.

*   **Goal:** Standardize the valuation process and speed up loan approvals.
*   **Features:**
    *   GPS-tagged photo uploads of the vehicle (exterior, interior, engine).
    *   Digital inspection checklist.
    *   Instant upload to the internal CRM to trigger the final loan offer.

## Phase 5: AI & Operations Scaling

### 🤖 AI-Powered Automation
To handle increased loan volume without drastically increasing operational headcount.

*   **Goal:** Eliminate manual data entry and scale sales/collections via Artificial Intelligence.
*   **Features:**
    *   **AI Document Processing (OCR):** Automatically extract names and vehicle numbers from uploaded IDs and logbook photos.
    *   **AI Voice Sales Agent:** A conversational bot to call users who abandon their applications at night.
    *   **AI Collections Agent:** Automated polite reminder calls for overdue payments.
