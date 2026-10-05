# TopPlate AI – SDLC Plan

*2 October 2026 · Thushan Wijesekara*

## Overview

TopPlate AI is a dish-discovery platform for Dubai: people search, rate and compare individual dishes, not just restaurants, and an AI assistant recommends the best plates for their budget, area and diet.

This plan takes it from idea to a live MVP in about 6 months, following the 7 SDLC phases. Prices are in AED; durations and costs are estimates to confirm during Planning.

**MVP goal:** 500 dishes from 150 restaurants in 3 areas (Al Karama, Deira, JBR), with search, ratings, reviews and the AI chat assistant.

---

## Phase 1: Planning (2 weeks)

Decide whether TopPlate AI is worth building and what the first version includes.

- **Market research:** study competitors (Zomato, Talabat reviews, Google Maps, Instagram food pages). The gap: none rank individual dishes.
- **Target users:** UAE residents, tourists, office workers looking for lunch, food bloggers.
- **Business model:** featured restaurant listings, sponsored dishes, ads, later a premium user tier.
- **Feasibility:** budget, team, timeline and legal needs (trade licence, UAE data protection law).
- **Brand:** domain (.com and .ae), social handles, UAE trademark.

**Deliverables:** project charter, budget estimate, risk list, go/no-go decision.

## Phase 2: Requirements (3 weeks)

### Functional requirements (MVP)

| Feature | What it does | Priority |
|---|---|---|
| Dish search | By name, cuisine, price (AED), rating, spice level, area | Must |
| Dish pages | Photo, price, restaurant, rating, reviews | Must |
| Ratings and reviews | Rate dishes 1–5 and write reviews | Must |
| AI chat assistant | Recommends dishes from the database by budget and preference | Must |
| User accounts | Email, Google or Apple; UAE Pass later | Must |
| Dietary filters | Halal, vegetarian, vegan, gluten-free | Must |
| Compare dishes | Side-by-side view of 2–3 dishes | Should |
| Trending dishes | Most-reviewed in the last 7 days | Should |
| Restaurant menus | Full menu with prices | Should |
| Restaurant portal | Owners update menus and reply to reviews | Later |
| Arabic language | Full Arabic interface | Later |

### Non-functional requirements

- Search results in under 2 seconds; AI replies in under 5 seconds.
- Mobile first (iOS, Android, mobile web).
- Compliant with UAE data protection law (PDPL); user data stored securely.
- Fake-review protection: one review per user per dish, reporting and moderation.

**Deliverables:** SRS, user stories, acceptance criteria.

## Phase 3: Design (4 weeks)

**UI/UX:** wireframes, then high-fidelity Figma screens (home, search results, dish page, AI chat, compare, profile); clickable prototype tested with 10–15 Dubai users; brand kit.

### Tech stack

| Layer | Choice | Why |
|---|---|---|
| Mobile app | Flutter or React Native | One codebase for iOS and Android |
| Web app | Next.js | Fast, good for search engines |
| Backend API | Node.js or Python (FastAPI) | Common, easy to hire for |
| Database | PostgreSQL (e.g. Supabase) | Dishes, restaurants, users, reviews |
| Search | PostgreSQL full-text or Algolia | Fast filtered search |
| AI assistant | Claude API with tool calls to the dish database | Answers from real data, not guesses |
| Images | Cloud storage + CDN | Fast dish photos |
| Maps | Google Maps API | Area and distance filters |
| Hosting | AWS me-central-1 (UAE) or Azure UAE | Keeps data in the UAE |

**Core data model:** Restaurant, Dish, User, Review, Rating, Area, Cuisine, DietaryTag.

**Deliverables:** Figma designs, architecture document, database schema, API specification.

## Phase 4: Development (10 weeks)

2-week Agile sprints with a demo at the end of each.

| Sprint | Weeks | Build |
|---|---|---|
| 1 | 1–2 | Project setup, database, sign-up and login |
| 2 | 3–4 | Restaurant and dish data, admin panel |
| 3 | 5–6 | Search and filters (price, area, cuisine, spice, diet) |
| 4 | 7–8 | Ratings, reviews, trending and compare |
| 5 | 9–10 | AI chat assistant connected to the dish database |

**In parallel:** a small team collects 500 dishes with prices and photos in Al Karama, Deira and JBR.
**Practices:** Git, code reviews, automated builds, staging server for each demo.

**Deliverables:** working MVP on staging, admin panel, seeded dish database.

## Phase 5: Testing (3 weeks)

| Test type | What is checked |
|---|---|
| Unit and integration | Each feature and API works alone and together |
| Functional | Every user story meets its acceptance criteria |
| AI quality | 100 test questions; answers use only real dishes, correct prices and areas |
| Performance | Search < 2 s and AI < 5 s with 1,000 concurrent users |
| Security | Login, data protection, review abuse, API access |
| Device | Popular iPhones and Android phones, small and large screens |
| UAT | 1-week beta with 50–100 Dubai users |

**Exit rule:** no critical or high bugs open, and beta users rate the app 4/5 or better.

## Phase 6: Deployment (2 weeks)

1. Production servers in the UAE region, with backups and monitoring.
2. Submit to the App Store and Google Play.
3. Soft launch in Al Karama, Deira and JBR.
4. Launch marketing: food bloggers, Instagram creators, "Rated on TopPlate" restaurant stickers.
5. Monitor errors, speed and sign-ups daily for 2 weeks.

**Deliverables:** live apps and website, launch checklist, rollback plan.

## Phase 7: Maintenance and growth (ongoing)

- **Support:** bug fixes, price and menu updates, review moderation.
- **Monitor:** uptime, crashes, AI answer quality, monthly active users, reviews per week.
- **Improve:** releases every 2–4 weeks based on feedback.
- **Expand:** Downtown, Business Bay, Jumeirah, Dubai Marina, then Abu Dhabi and Sharjah.
- **Next features:** Arabic interface, restaurant portal, UAE Pass login, delivery links, dish photo recognition.

**KPIs for the first 6 months:** 10,000 users, 5,000 reviews, 1,500 dishes, 30 paying restaurant partners.

## Timeline, team and budget

The MVP takes about **24 weeks** from kickoff to public launch.

| Role | People |
|---|---|
| Project manager / product owner | 1 |
| UI/UX designer | 1 |
| Mobile and web developers | 2 |
| Backend and AI developer | 1 |
| QA tester | 1 |
| Data collectors (part-time) | 2–3 |
| Marketing lead | 1 |

| Item | Estimated cost (AED) |
|---|---|
| Design and development | 150,000 – 400,000 |
| Dish data collection and photos | 15,000 – 30,000 |
| Brand, legal and trade licence | 20,000 – 50,000 |
| Launch marketing | 30,000 – 80,000 |
| **MVP total** | **215,000 – 560,000** |
| Running costs (hosting, AI API, Maps) | 3,000 – 10,000 / month |
