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
```markdown
# Wildverse — Product Specification

Public product specification for the Wildverse ecosystem.

This document defines what Wildverse offers and the user-facing rules of the experience.

---

## 1. Vision

Make healthier, smarter and more sustainable living effortless and fun by combining AI scanners with an evolving AR companion that rewards real-world positive actions.

## 2. Target users

- Health-conscious consumers.
- Budget-aware households.
- AR and collection game players.
- Local businesses and brands.

## 3. AR ecosystem

- AI-driven companions.
- Eggs and hatching mechanics.
- 3D collection system.
- Real-world AR interactions.

## 4. AI scanners
Scanner	Inputs	Output
Food	Photo / barcode / text	Nutrition score, health analysis, alternatives
Product	Photo / barcode	Ingredient analysis, safety alerts
Cosmetic	Photo / barcode	Allergens, irritants, compatibility
Receipt	Receipt image	Expenses, categories, budget insights
Rules:

Every scan returns a structured result.
Known items are processed faster through shared knowledge.
Scans contribute XP.
5. Lifestyle intelligence
Includes:

Daily missions.
Streaks.
Achievements.
Weekly summaries.
Personalized recommendations.
6. Evolution mechanics
XP-based progression.
Multiple evolution stages.
Unlockable visuals and abilities.
Seasonal and sponsored events.
7. Partner ecosystem
Partners can access:

Self-service onboarding.
Sponsored companions.
Sponsored missions.
Analytics dashboards.
Subscription plans.
8. AI discoverability
Wildverse supports:

Public llms.txt
AI-friendly robots.txt
XML sitemap
JSON-LD structured data
CitableHub profile
9. Platforms & availability
Web (PWA)
iOS
Android
Primary market:

United States
Default language:

English
10. Privacy & trust
Users can export data.
Users can delete data.
Role separation between users, partners and admins.
Communication limits to prevent fatigue.
Legal references:

Privacy Policy
Terms of Service
Refund Policy
11. Out of scope
This document intentionally excludes:

Source code
Database schemas
API keys
Internal prompts
Proprietary algorithms
Private business logic
Privacy policy and legal compliance.
