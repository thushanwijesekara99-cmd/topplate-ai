# TopPlate AI 🍽️

**Rate the dish, not just the restaurant.** A dish-discovery platform for Dubai with an AI assistant that recommends the best plates for your budget, area and diet.

![Status](https://img.shields.io/badge/status-design%20%26%20planning-yellow)
![AI](https://img.shields.io/badge/AI-Claude%20API-D97757)
![Region](https://img.shields.io/badge/region-Dubai%2C%20UAE-red)

<!-- Add the home-page design and AI chat screen here -->
<!-- ![Home](docs/screenshots/home.png) -->

---

## The problem

Zomato, Talabat, Google Maps and Instagram food pages all review **restaurants**. But people order **dishes**. There's no easy way to find "the best chicken biryani under AED 30 in Karama" or compare two shawarmas side by side.

## The idea

TopPlate AI ranks individual dishes. People search, rate and compare plates, and an AI assistant answers questions like:

> *"Spicy vegetarian lunch in Deira under AED 25?"*

…using only real dishes, prices and locations from the database — not guesses.

## MVP scope

**500 dishes from 150 restaurants** in Al Karama, Deira and JBR.

| Feature | Priority |
|---|---|
| Dish search — name, cuisine, price (AED), rating, spice level, area | Must |
| Dish pages — photo, price, restaurant, rating, reviews | Must |
| Ratings & reviews (1–5) with fake-review protection | Must |
| AI chat assistant grounded in the dish database | Must |
| Accounts — email, Google, Apple (UAE Pass later) | Must |
| Dietary filters — halal, vegetarian, vegan, gluten-free | Must |
| Compare 2–3 dishes side by side | Should |
| Trending dishes (last 7 days) | Should |
| Restaurant portal, Arabic interface | Later |

## Proposed architecture

| Layer | Choice | Why |
|---|---|---|
| Mobile | Flutter or React Native | One codebase for iOS + Android |
| Web | Next.js | Fast, SEO-friendly |
| API | Node.js or Python (FastAPI) | Common, easy to hire for |
| Database | PostgreSQL (Supabase) | Dishes, restaurants, users, reviews |
| Search | Postgres full-text or Algolia | Fast filtered search |
| AI | Claude API with tool calls to the dish DB | Answers from real data |
| Maps | Google Maps API | Area and distance filters |
| Hosting | AWS me-central-1 (UAE) | Data stays in the UAE (PDPL) |

**Core data model:** Restaurant · Dish · User · Review · Rating · Area · Cuisine · DietaryTag

**Targets:** search < 2 s, AI reply < 5 s, at 1,000 concurrent users.

## Delivery plan (SDLC)

A 24-week plan from idea to public launch:

| Phase | Weeks | Output |
|---|---|---|
| 1. Planning | 2 | Market research, business model, go/no-go |
| 2. Requirements | 3 | SRS, user stories, acceptance criteria |
| 3. Design | 4 | Figma screens, architecture, DB schema, API spec |
| 4. Development | 10 | 5 Agile sprints → working MVP |
| 5. Testing | 3 | Functional, AI quality (100 test questions), performance, UAT beta |
| 6. Deployment | 2 | App Store, Google Play, web; soft launch in 3 areas |
| 7. Maintenance | ongoing | Expand to Downtown, Marina, Abu Dhabi, Sharjah |

Full plan, team and budget: [docs/SDLC-plan.md](docs/SDLC-plan.md)

## Business model

Featured restaurant listings · sponsored dishes · ads · premium user tier (later)

## Author

**Thushan Wijesekara** — product concept, requirements, SDLC planning and UI design
📧 thushanwijesekara99@gmail.com

## License

MIT — see [LICENSE](LICENSE).
