``markdown
# Wildverse — Architecture Overview

This document describes the public, high-level architecture of the Wildverse ecosystem.

Implementation details, source code, credentials and proprietary business logic are intentionally omitted.

---

## 1. System layers

```text
┌──────────────────────────────────────────────────────────────┐
│ Client (PWA + Mobile)                                        │
│ React · TypeScript · Tailwind · Capacitor · WebGL/AR layer   │
└───────────────┬─────────────────────────────┬────────────────┘
                │                             │
                ▼                             ▼
┌──────────────────────────┐   ┌────────────────────────────┐
│ Managed Backend (Cloud)  │   │ AI Gateway (multi-model)   │
│ Auth · DB · Storage      │   │ Vision · LLM · Embeddings  │
│ Edge functions · RLS     │   │                            │
└──────────────┬───────────┘   └──────────────┬─────────────┘
               │                              │
               ▼                              ▼
┌──────────────────────────────────────────────────────────────┐
│ Intelligence Services                                       │
│ Scanners · Recommendations · Agents · Analytics             │
│ Partner Platform · Notifications                            │
└──────────────────────────────────────────────────────────────┘
2. Client
Progressive Web App with offline caching and installable shortcuts.
Native shell via Capacitor.
AR companion layer rendered with WebGL/Three.js.
Accessible design system and responsive UI.
3. Managed backend
Provides:

Authentication and authorization.
Relational database with row-level security.
Object storage.
Edge functions for orchestration.
4. AI scanner pipeline
text
Copy
Image / Barcode
        ↓
Vision Model
        ↓
Knowledge Lookup
        ↓
LLM Reasoning
        ↓
Structured Result + Recommendations + XP
Results are cached for consistency and performance.

5. AR companion & evolution
XP earned through real-world activity.
Evolution stages driven by progression.
Conversational AI layer.
Data-driven rarity and abilities.
6. Lifestyle intelligence
Daily missions.
Smart recommendations.
Streaks and achievements.
Weekly summaries.
7. Partner ecosystem
Business onboarding portal.
Sponsored experiences.
Analytics dashboards.
Context-aware promotions.
8. AI discoverability layer
Wildverse includes:

llms.txt
robots.txt
XML sitemap
JSON-LD structured data
External AI citation profiles
9. Security & privacy
Row-level security.
Signed URLs.
Least-privilege data access.
Privacy policy and legal compliance.
