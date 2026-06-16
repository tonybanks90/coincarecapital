# System Architecture

This document details the planned infrastructure for the Coin Care Capital digital platform, transitioning from the current static prototype to a dynamic, scalable system.

## High-Level Architecture (Proposed)

We are adopting a MACH (Microservices, API-first, Cloud-native SaaS, Headless) architecture.

```mermaid
graph TD
    %% Define styles
    classDef frontend fill:#3b82f6,stroke:#1e3a8a,stroke-width:2px,color:#fff;
    classDef content fill:#ec4899,stroke:#be185d,stroke-width:2px,color:#fff;
    classDef backend fill:#10b981,stroke:#047857,stroke-width:2px,color:#fff;
    classDef mobile fill:#8b5cf6,stroke:#6d28d9,stroke-width:2px,color:#fff;

    %% Nodes
    Web[Next.js Web App]:::frontend
    MobileApp[React Native Mobile App]:::mobile
    Sanity[(Sanity.io Headless CMS)]:::content
    API[Node.js / Python Secure API]:::backend
    DB[(PostgreSQL / Supabase)]:::backend
    ThirdParty[eCitizen / NTSA API Integration]:::backend
    
    %% Relationships
    Web <-->|Fetch content via GROQ| Sanity
    Web <-->|Submit Loan App via REST/GraphQL| API
    
    MobileApp <-->|Fetch content via GROQ| Sanity
    MobileApp <-->|Submit Loan App, Track Status| API
    
    API <-->|Store PII & Loan Logic| DB
    API <-->|Verify Logbook Status| ThirdParty
```

## Data Separation Strategy

1.  **Public Content (Sanity CMS):** 
    *   Blog Posts
    *   FAQs
    *   Marketing copy (Hero text, About Us)
    *   Branch locations
2.  **Private/Transactional Data (Custom Backend/Supabase):**
    *   User Profiles (Name, M-Pesa Number)
    *   Vehicle Registration Data
    *   Loan Application Status (Pending, Approved, Disbursed)
    *   Repayment Ledgers

## Next Steps for CMS Integration
1. Initialize a Sanity Studio in `Coin-Care/studio`.
2. Define the Schema types (e.g., `document { name: 'faq', type: 'document', fields: [...] }`).
3. Replace the mock data in `frontend/src/data` with Sanity `fetch` calls using GROQ.
