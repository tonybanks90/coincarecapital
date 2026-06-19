# Project Proposal & Scope of Work

**Project:** Coin Care Capital — Digital Platform\
**Client:** Coin Care Capital LTD\
**Developer:** Antony Ndumia\
**Date:** 6/16/2026\
**Version:** 1.0

***

## 1. Executive Summary

This document outlines the scope, deliverables, timeline, and investment for the design, development, and deployment of the **Coin Care Capital** digital platform — a modern, high-performance website that serves as the company's primary tool for **customer acquisition**, **loan application processing**, **brand credibility**, and **content marketing** in the Kenyan logbook loan market.

***

## 2. Project Objectives

| # | Objective                                       | Success Metric                                             |
| - | ----------------------------------------------- | ---------------------------------------------------------- |
| 1 | Generate qualified loan leads online            | Number of completed "Apply Now" form submissions per month |
| 2 | Establish brand authority and trust             | Bounce rate < 40%, average session duration > 2 minutes    |
| 3 | Educate potential borrowers                     | Blog traffic, FAQ engagement, calculator usage             |
| 4 | Enable self-service loan estimation             | Loan calculator usage rate                                 |
| 5 | Provide a direct WhatsApp communication channel | Click-through rate on WhatsApp CTAs                        |
| 6 | Allow non-technical staff to update content     | CMS adoption (blog posts published, FAQs updated)          |

***

## 3. Scope of Work

### 3.1 What Is Included (In Scope)

#### Phase 1: Website Design & Development

* [x] Custom responsive website design (mobile-first)
* [x] Home page with hero section, about us, loan process, B2B section, FAQs
* [x] About page
* [x] Blog listing page + individual blog post pages
* [x] Requarement for loan (interactive)
* [x] Contact page
* [x] Multi-step loan application modal (Apply Now)
* [x] WhatsApp integration (click-to-chat)
* [x] Sticky navigation bar with mobile hamburger menu
* [x] Professional footer with contact details and CTA

#### Phase 2: Content Management System (CMS)

* [x] Sanity CMS setup and configuration
* [x] Admin panel accessible at `/admin` (no separate login needed)
* [x] Content types: Blog Posts, FAQs, Site Settings
* [x] Ability to update hero tagline, interest rates, and WhatsApp URL without developer help
* [x] Image management for blog posts

#### Phase 3: Deployment & Launch

* [x] Premium cloud hosting setup and configuration
* [x] Custom domain connection (coincarecapital.co.ke or similar)
* [x] SSL certificate (HTTPS for secure browsing)
* [x] SEO meta tags and Open Graph setup
* [x] Performance optimization (target Lighthouse score > 90)
* [x] Google Analytics / Tag Manager integration

#### Phase 4: Documentation & Handover

* [x] CMS user guide (how to add blog posts, edit FAQs, change settings)
* [x] Technical documentation for future developers
* [x] 30-day post-launch support period

### 3.2 Optional Add-Ons (Available Now)

> \[!IMPORTANT] The following items are **not** included in the core project investment, but they can be quoted separately and executed immediately alongside the website build to accelerate your launch.

* 🎨 **Content Creation Factory:** A built-in tool at `/studio` that lets your team generate professional, on-brand social media posts (holidays, promotions, news), flyers, and branded company documents in 3 simple steps — customize, download, and share. No graphic designer needed.
* 🎨 **Social Media Content & Banners:** Custom, high-converting graphics for Facebook, Instagram, X, and TikTok.
* ✉️ **Email & SMS Marketing Setup:** Automated customer retention campaigns (e.g., "Complete your application" or "Happy Birthday").
* ✍️ **Ongoing Content Writing:** SEO-optimized blog posts written and published weekly.
* 📸 **Brand Identity & Media:** Professional logo design, brand guidelines, and corporate photography/video production.

### 3.3 Proposed Future Phases (The Scaling Strategy)

To ensure Coin Care Capital can handle high loan volumes without dramatically increasing staff headcount, we propose the following post-launch phases (detailed further in our Internal Tools & Scaling documentation):

* **Phase 1: Loan Processing Backend & CRM:** A centralized internal dashboard to track loans, approve workflows, and automate M-Pesa/Bank disbursements.
* **Phase 2: The Mobile App (iOS / Android):** A dedicated application with user accounts, secure login, and push notifications for repeat borrowers.
* **Phase 3: Government API Integrations:** Direct connection to NTSA / eCitizen for instant, automated logbook verification.
* **Phase 4: AI-Powered Features:** Implementing OCR to automatically extract data from uploaded IDs, and deploying AI Voice Sales Agents to call customers who abandon their applications.

***

## 4. Technology Stack

| Component          | Technology                                         | Why                                                               |
| ------------------ | -------------------------------------------------- | ----------------------------------------------------------------- |
| Frontend Framework | Next.js 16 (React 19)                              | Server-side rendering for SEO, fast page loads, modern React      |
| Styling            | Tailwind CSS v4                                    | Rapid, consistent, responsive design                              |
| Animations         | Framer Motion                                      | Smooth, professional micro-interactions                           |
| Icons              | Lucide React                                       | Consistent, lightweight icon set                                  |
| CMS                | Sanity.io                                          | Real-time editing, flexible content modeling, free tier available |
| Hosting            | Premium Cloud Hosting                              | Optimized for Next.js, auto-scaling, global CDN, free SSL         |
| Version Control    | [GitHub](https://github.com/Coin-Care-Capital-LTD) | Code backup, collaboration, deployment pipeline                   |

***

## 5. Deliverables Checklist

| #  | Deliverable                               | Format                                             | Delivered When     |
| -- | ----------------------------------------- | -------------------------------------------------- | ------------------ |
| 1  | This Project Proposal & SOW               | PDF/Markdown                                       | Before work begins |
| 2  | Sitemap & Feature Breakdown               | PDF/Markdown                                       | Week 1             |
| 3  | Wireframes / UI Mockups                   | Figma / Image files                                | Week 1             |
| 4  | Design System (colors, fonts, components) | Document                                           | Week 1             |
| 5  | Functional website (staging URL)          | Live URL                                           | Week 1             |
| 6  | CMS setup with sample content             | Live admin panel                                   | Week 2             |
| 7  | Production deployment (live URL)          | Live URL                                           | Week 2             |
| 8  | CMS User Guide                            | PDF/Markdown                                       | Week 2             |
| 9  | Technical Documentation                   | Markdown (GitBook)                                 | Week 2             |
| 10 | Source code repository access             | [GitHub](https://github.com/Coin-Care-Capital-LTD) | Week 2             |

***

## 6. Investment & Payment Schedule

Building a high-performance, custom-coded financial platform (Next.js + Headless CMS) is an investment in your primary customer acquisition channel. Unlike standard template websites, this architecture ensures maximum speed, military-grade security, and scalable infrastructure.

### 6.1 Project Cost Breakdown (One-Time Setup)

| Phase                       | Description                                                                                            | Cost (KES) |
| --------------------------- | ------------------------------------------------------------------------------------------------------ | ---------- |
| **1. UI/UX & Strategy**     | User journey mapping, wireframes, and custom design layouts tailored for conversion.                   | 10,000     |
| **2. Frontend Engineering** | Custom Next.js development, responsive mobile-first architecture, and the multi-step "Apply Now" flow. | 25,000     |
| **3. Backend & CMS**        | Sanity Headless CMS configuration for seamless blog and FAQ management.                                | 12,000     |
| **4. Deployment & SEO**     | Server setup, technical SEO implementation, analytics tracking, and technical handover.                | 8,000      |
|                             | **Total Project Investment**                                                                           | **55,000** |

### 6.2 Domain, Hosting & Maintenance (Recurring)

To keep the platform running securely and smoothly 24/7, the following recurring costs apply:

| Service                            | Description                                                                                                              | Cost (KES)        |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ----------------- |
| **Custom Domain**                  | Annual registration (e.g., .co.ke)                                                                                       | \~2,500 / year    |
| **Hosting & Maintenance Retainer** | Cloud server costs, SSL renewals, monthly backups, CMS updates, and up to 1 hour of technical support/updates per month. | **5,000 / month** |

_(Note: The first month of hosting is included in the project investment. Recurring billing starts 30 days after launch)._

### 6.3 Payment Milestones

To ensure alignment and momentum, the investment is divided into three milestones linked directly to project deliverables:

| Milestone             | Trigger                                           | Amount (KES) | Due Date           |
| --------------------- | ------------------------------------------------- | ------------ | ------------------ |
| **Deposit (40%)**     | Signed SOW + project kickoff                      | **22,000**   | Before work begins |
| **Milestone 1 (30%)** | Approval of UI designs + Delivery of staging site | **16,500**   | End of Week 1      |
| **Milestone 2 (30%)** | Production launch, CMS training + Handover        | **16,500**   | End of Week 2      |

***

## 7. Revision Policy

* **Design phase:** Up to **3 rounds** of revisions on the overall design direction.
* **Development phase:** Up to **2 rounds** of revisions on the implemented design.
* **Content changes:** Unlimited minor content updates (text, images) via the CMS after handover.
* **Structural changes** (adding new pages, new features, layout overhauls) after approval of the design are billed at an hourly rate of **KES \[Rate]/hour**.

***

## 8. Client Responsibilities

For this project to succeed, the client agrees to provide:

1. **Brand assets** — Logo files (SVG/PNG), brand colors (if established), any existing marketing materials
2. **Written content** — Company description, team bios, service descriptions, FAQ answers (see Content Requirements document)
3. **Photography** — Office photos, team photos, vehicle images (or approval to use stock/AI-generated images)
4. **Domain access** — DNS credentials for connecting the custom domain
5. **Timely feedback** — Respond to design reviews and questions within **3 business days** to keep the project on schedule
6. **Single point of contact** — Designate one decision-maker to avoid conflicting feedback

***

## 9. Ownership & Intellectual Property

* Upon final payment, the client receives **full ownership** of all custom code, designs, and content created for this project.
* The developer retains the right to showcase the project in their portfolio unless the client objects in writing.
* Third-party tools and services (Next.js, Sanity, etc.) are subject to their own licensing terms.

***

## 10. Agreement

By signing below, both parties agree to the terms outlined in this Scope of Work.

|               | Client                                             | Developer                                          |
| ------------- | -------------------------------------------------- | -------------------------------------------------- |
| **Name**      | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Antony Ndumia                                      |
| **Title**     | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Lead Developer                                     |
| **Signature** | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| **Date**      | \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | 6/16/2026                                          |
