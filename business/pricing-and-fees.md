# Pricing & Fee Structure

This document outlines the business logic for calculating loan limits, interest rates, and penalties at Coin Care Capital. These formulas dictate the math behind the Loan Calculator and the future backend ledger.

## 1. Loan-To-Value (LTV) Cap

We do not lend the full value of the vehicle. We lend a percentage based on the vehicle's age and condition to mitigate depreciation risk.

*   **Standard Max LTV:** 60% of the forced sale value (FSV).
*   **Age Penalty:** Vehicles over 10 years old have a reduced max LTV of 40%.

**Formula:**
`Max Loan Amount = Vehicle Valuer FSV * LTV %`

*Example:* A 2018 Mazda Demio valued at KES 800,000 (FSV) qualifies for a maximum loan of KES 480,000.

## 2. Interest Rates

Interest is calculated on a **flat rate** per month.

*   **Standard Rate:** 3.5% per month.
*   **Preferred Client Rate:** 2.5% per month (For returning clients with zero late payments on previous loans).
*   **High-Risk Rate:** 5.0% per month (For older vehicles or high-risk profiles).

**Formula (Flat Rate):**
`Total Interest = Principal * Monthly Interest Rate * Tenure in Months`
`Monthly Installment = (Principal + Total Interest) / Tenure in Months`

*Example:* 
*   Principal: KES 100,000
*   Rate: 3.5% per month
*   Tenure: 12 months
*   Total Interest = 100,000 * 0.035 * 12 = KES 42,000
*   Monthly Installment = 142,000 / 12 = KES 11,833.33

## 3. Processing Fees

A one-off fee deducted directly from the disbursed principal before it reaches the customer's account.

*   **Valuation Fee:** KES 3,500 (Often paid upfront by the client to the valuer, or deducted if done in-house).
*   **Processing Fee:** 3% of the Principal amount.
*   **NTSA Joint Registration Fee:** Passed on to the customer (approx. KES 1,050).
*   **Tracking Installation (If applicable):** KES 5,000.

## 4. Default Penalties & Repossession

To encourage timely payments:
*   **Grace Period:** 3 Days post due-date.
*   **Late Payment Penalty:** 5% of the overdue installment amount, applied on day 4.
*   **Roll-over:** If a client misses a full month, the overdue interest compounds, but the principal does not.
*   **Repossession Trigger:** 60 Days in arrears triggers vehicle tracking recovery and clamping. Repossession costs (auctioneer fees, towing) are added to the loan balance.
