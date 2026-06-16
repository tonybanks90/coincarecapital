# API Contracts

This document outlines the RESTful API endpoints required to power the web frontend, specifically focusing on the newly prioritized **Loan Tracker** and the **Loan Application** flow.

## Base URL
`https://api.coincarecapital.co.ke/v1`

## Authentication
Most endpoints require a Bearer token (JWT) obtained via OTP login. The initial public application endpoint does not require auth.

---

## 1. Authentication Endpoints

### Request OTP
Trigger an SMS OTP to the user's phone.
*   **Endpoint:** `POST /auth/request-otp`
*   **Body:**
    ```json
    { "phone_number": "+254720078432" }
    ```
*   **Response (200 OK):**
    ```json
    { "status": "success", "message": "OTP sent." }
    ```

### Verify OTP
Exchange the OTP for a JWT session token to access the Loan Tracker.
*   **Endpoint:** `POST /auth/verify-otp`
*   **Body:**
    ```json
    { "phone_number": "+254720078432", "otp": "4819" }
    ```
*   **Response (200 OK):**
    ```json
    { "token": "eyJhbGciOiJIUzI...", "user_id": "uuid-1234" }
    ```

---

## 2. Loan Tracker Endpoints (Authenticated)

### Get Active Loans
Fetches the user's active loans to populate the tracker dashboard.
*   **Endpoint:** `GET /loans/active`
*   **Headers:** `Authorization: Bearer <token>`
*   **Response (200 OK):**
    ```json
    {
      "data": [
        {
          "loan_reference": "L-2026-8921",
          "status": "ACTIVE",
          "principal": 250000,
          "balance_remaining": 145000,
          "next_payment": {
            "due_date": "2026-07-01",
            "amount": 25000
          },
          "progress_percentage": 42
        }
      ]
    }
    ```

### Get Application Status
For users whose loan is still processing.
*   **Endpoint:** `GET /loans/status/{loan_reference}`
*   **Headers:** `Authorization: Bearer <token>`
*   **Response (200 OK):**
    ```json
    {
      "status": "PENDING_VALUATION",
      "steps": [
        { "name": "Application Received", "completed": true },
        { "name": "Valuation Scheduled", "completed": false },
        { "name": "NTSA Transfer", "completed": false },
        { "name": "Disbursement", "completed": false }
      ]
    }
    ```

---

## 3. Public Endpoints

### Submit New Loan Application
Called when the user completes the 3-step Apply Now modal on the frontend.
*   **Endpoint:** `POST /loans/apply`
*   **Body:**
    ```json
    {
      "full_name": "John Doe",
      "phone_number": "0720078432",
      "vehicle_registration": "KDC 123X",
      "vehicle_make": "Toyota"
    }
    ```
*   **Response (201 Created):**
    ```json
    {
      "status": "success",
      "loan_reference": "L-2026-9001",
      "message": "Application received. A valuer will contact you shortly."
    }
    ```
