# Mobile Application Roadmap

To scale Coin Care Capital and provide a seamless self-service experience, we plan to launch native mobile applications for iOS and Android.

## Technology Stack Recommendation: React Native / Expo
Because our web platform is built on React (Next.js), adopting **React Native** (specifically via the **Expo** framework) is the most efficient path forward. It allows us to share business logic, UI patterns (via Tailwind Native or similar), and development resources between web and mobile.

## Phased Approach

### Phase 1: The "Lite" App (Lead Generation & Tracking)
*   **Core Feature:** Submit a loan application via a mobile-optimized multi-step form.
*   **Core Feature:** "Check My Loan Status" dashboard.
*   **Core Feature:** Simple loan calculator.
*   **Goal:** Get a presence on the App Store and Play Store quickly.

### Phase 2: The "Self-Service" App (Account Management)
*   **Core Feature:** Secure login (OTP via SMS).
*   **Core Feature:** View active loans, remaining balance, and repayment schedule.
*   **Core Feature:** Make payments directly via M-Pesa STK Push API integration within the app.
*   **Core Feature:** Push notifications for payment reminders.

### Phase 3: The "Valuation" App (Internal Agent App)
*   A separate, internal-only app for Coin Care Valuation Officers.
*   **Features:** GPS tracking, camera integration for uploading vehicle condition photos, instant sync with the CRM/Backend to generate loan offers on the spot.

## Directory Structure Strategy
As we scale, we will adopt a Monorepo strategy (e.g., using Turborepo):
*   `/apps/web` (Current Next.js app)
*   `/apps/mobile` (Expo React Native app)
*   `/apps/studio` (Sanity CMS)
*   `/packages/ui` (Shared React components, buttons, icons)
*   `/packages/config` (Shared Tailwind config, ESLint)
