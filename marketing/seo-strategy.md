# SEO & Content Strategy

To ensure Coin Care Capital ranks high on Google for relevant search terms in Kenya (e.g., "logbook loans Nairobi", "cash against logbook", "fast loans Kenya"), we must adhere to a strict SEO strategy.

## 1. Technical SEO Configuration (Next.js)

The current web application utilizes Next.js App Router, which provides excellent SSR (Server-Side Rendering) out of the box, ensuring search engines can perfectly read our content.

*   **Metadata API:** Each page uses the `export const metadata` object for unique titles and descriptions.
*   **Dynamic Routes:** The blog uses dynamic routes (`/blog/[slug]`) to generate unique pages for every article.
*   **Semantic HTML:** We use `<h1>` (only once per page), `<h2>`, `<h3>`, and `<section>` tags to structure content logically.
*   **Performance:** Image optimization via `next/image` ensures fast LCP (Largest Contentful Paint) scores, a crucial Google ranking factor.
*   **Sitemap & Robots.txt:** Must be dynamically generated via Next.js to ensure all blog posts are instantly indexed.

## 2. Keyword Strategy

Our keyword research is focused on intent-driven searches specific to the Kenyan market.

*   **Transactional Keywords (High Intent):** 
    *   `logbook loans in nairobi`
    *   `cash against car logbook`
    *   `car title loans kenya`
    *   `loans without crb check kenya`
*   **Informational Keywords (Medium Intent):** 
    *   `how to calculate logbook loan interest`
    *   `logbook loan requirements in kenya`
    *   `what happens if i default on a logbook loan`
*   **Local SEO:** 
    *   Setting up and optimizing the **Google Business Profile**.
    *   Ensuring consistent NAP (Name, Address, Phone) across local directories (Yellow Pages Kenya, Foursquare, etc.).

## 3. Blog Content Pillars

The blog (`/blog`) is the primary driver for capturing informational keywords. By answering questions users are googling, we build trust and redirect them to the loan application.

*   **Pillar 1: Financial Education & Business Growth**
    *   Targeting SMEs. e.g., "How to use asset finance to scale your delivery business."
*   **Pillar 2: The Loan Process Explained**
    *   Transparency builds trust. e.g., "Step-by-step: How vehicle valuation works at Coin Care."
*   **Pillar 3: Vehicle Ownership in Kenya**
    *   Broad appeal topics. e.g., "How to check NTSA logbook transfer status on eCitizen."

## 4. Off-Page SEO (Backlink Strategy)

Domain Authority (DA) dictates how easily we rank. We need links from reputable Kenyan websites pointing to coincarecapital.co.ke.

*   **PR & News Sites:** Getting featured in Business Daily, Kenyans.co.ke, or Tuko.co.ke regarding SME financing trends.
*   **Automotive Blogs:** Guest posting on Kenyan car review websites or forums (e.g., Mashinani, KenyanTalk).
*   **Partner Links:** Ensuring any partnered valuers or insurance agencies link back to our site.

## 5. Ongoing Monitoring

*   **Google Search Console:** Track indexing errors, core web vitals, and exact search queries driving traffic.
*   **Google Analytics 4 (GA4):** Track user behavior, bounce rates, and conversion paths from specific blog posts to the Apply modal.
