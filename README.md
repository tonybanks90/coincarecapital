# Coin Care Capital - Internal Documentation

Welcome to the Coin Care Capital engineering and business documentation hub. This repository contains the source code for the Next.js web application and the foundational architecture for our future mobile and backend scaling.

## Directory Structure

*   **/frontend**: The Next.js 15 App Router web application (React, Tailwind CSS, Lucide Icons).
*   **/docs**: GitBook-style documentation.
    *   `/business`: Workflows, loan processing logic, and business rules.
    *   `/marketing`: SEO strategy, content guidelines.
    *   `/technical`: System architecture, CMS integration plans, Database schemas.
    *   `/scaling`: Mobile application roadmap (iOS/Android).

## Quick Start (Web App)

```bash
cd frontend
npm install
npm run dev
```

> [!NOTE]
> The web application currently runs with local structured data in `src/data`. This is in preparation for a headless CMS (Sanity) integration in Phase 3.
