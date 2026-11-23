# Uvision — MVP Beta

## Problem
People in France who need a photographer or videographer for a specific occasion (event, portrait, corporate shoot) find it slow and uncertain to hire one: they browse social networks or directories, ask for quotes, wait for answers and go back and forth before knowing the price or whether the creative is free. Meanwhile, emerging creatives, many of them students, struggle to be seen and to turn their work into paid bookings. Left unsolved, clients give up or settle for the first available option, and good creatives stay invisible.

## Evidence
- **Client side:** founders' observation — "reaching a creative remains complex, slow and uncertain". Assumption — needs validation via user testing with clients on the beta.
- **Creative survey, 50 respondents (Nov. 2026):** 69% cite lack of visibility as their main problem, 57% finding clients; 58% have no client yet; 69% do not find clients easily (36 answers); 66% use no platform, and those who do mostly use Instagram. Sample bias: 72% students, 46% illustration — only part of it is photo/video.
- **Respondent quote:** "Job search platforms are too poorly suited to artists."
- **Commission tolerance (survey):** 8% acceptable for 47%, 10% for 22%, 5% for 20%.
- **Launch interest (survey):** 92% want to be told when the platform opens.
- **Market (secondary analysis, sources not independently verified):** no French equivalent for consumers with on-platform booking and payment — only directories (Mariages.net, PhotoPresta) and B2B services (Utopix, Shoootin); Meero was ~95% B2B. Comparable models abroad: Snappr (closest), Lovegraph (Japan), SweetEscape, Flytographer, Perfocal. "64% of French couples find their suppliers on a specialised site or app" — single figure, source to confirm.
- **"Market not yet exploited in France":** Assumption — needs validation via market sizing (number of independent visual creatives, booking volume).

## Users
- **Primary**: the individual client in France with a one-off need (wedding, event, portrait, corporate, product…), a location and a budget, who wants to go from search to a paid booking without asking for a quote or waiting for an answer.
- **Secondary**: the visual creative — photographer, videographer or both, often a student or early-career independent — who needs to be found, show a portfolio, sell fixed-price services and get paid. Their storefront is what makes the client journey possible.
- **Not for (MVP)**: companies and brands (calls for tenders, casting), schools, creatives outside photo/video.

## Hypothesis
We believe **instant booking of a photographer or videographer — with portfolio, fixed prices, real availability and on-platform payment visible upfront** — will **remove the quote-and-wait friction of hiring a visual creative** for **individual clients in France**.
We'll know we're right when **clients who search go on to book and pay without contacting the creative first**, and **creatives get regular clients through the platform** (targets TBD — see Open Questions).

## Success Metrics
Project success (March 2027) is a working beta, ready to go to production. Product success is measured after launch.

| Metric | Target | How measured |
|---|---|---|
| End-to-end client journey works (search → profile → service and slot → booking → test payment → personal space) | 100% of steps pass | Automated end-to-end tests in a test environment |
| Client usability | TBD — share of test clients who complete a booking without help | Moderated user tests on the beta |
| Creative side ready to receive bookings (sign-up → storefront → booking received) | 100% of steps pass | Automated end-to-end tests |
| Production readiness | Security checklist and GDPR review passed, no open critical vulnerability | Security test report |
| Handover readiness | All end-of-project deliverables from the kick-off email present | Checklist review with the founders |
| *(post-launch)* Search-to-booking conversion | TBD | Booking analytics |
| *(post-launch)* Regular clients for creatives | TBD — e.g. share of creatives with ≥ N bookings per month | Booking analytics |

## Scope
**MVP** — A beta that a client and a creative can use end to end in a test payment environment, across **all of France** and **all twelve categories** (Events, Sport, Corporate / Business, Fashion & Portrait, Real estate, Products / E-commerce, Lifestyle / Social media, Photobooth, Video / film production, Drone, Travel / nature, Technical / specialised):
- Client side: search by category, location (city or postcode), budget, type of professional and name; **advanced filters** (availability, rating and reviews, equipment, extra services, travel area); profile card and full profile; booking of a service and slot; payment on the platform (deposit or full amount, with balance and due dates shown upfront); email confirmation; booking tracking in a personal space; **reviews**, open to any client whose booking is confirmed.
- Creative side: sign-up and sign-in, light verification (phone, identity check through the payment provider in test mode), profile, portfolio, services with fixed prices, availability calendar, configurable deposit (on/off, fixed or percentage, per service, refund conditions), booking tracking in a personal space.
- Both: **in-platform messaging** between client and creative.
- Interface in French and English.
- Commission: 5% on bookings.

**Out of scope**
- Validation code at the end of the session — post-MVP; payment release rule to be revisited (photos are delivered after the session).
- SMS confirmation, SIRET check, two-factor authentication — post-MVP verification hardening.
- Interactive map and geolocation — search by city or postcode first.
- Graine de Champion gamification, Uvision Award, Uvision Ads — growth features, after the core journey is proven.
- Company and School accounts, calls for tenders, casting — other segments.
- Other visual professions, AI recommendations, international — expansion.
- Favourites, FAQ, blog, partners page, yearly recap, comparison, Behance link, promo codes, account deactivation — secondary.
- Manual quality curation of creatives — not in MVP (requires an admin back office); see Risks.

## Delivery Milestones
<!-- Business outcomes, not engineering tasks. /plan turns each into a plan. -->
<!-- Status: pending | in-progress | complete -->

| # | Milestone | Outcome | Status | Plan |
|---|---|---|---|---|
| 1 | Creative storefront | A creative signs up, passes light verification and publishes a profile with portfolio, priced services, availability and deposit settings — the supply the client journey needs | pending | — |
| 2 | Find a creative | A client anywhere in France finds creatives by category, location, budget, type and name, refines with advanced filters, and opens a full profile | pending | — |
| 3 | Book and pay | A client books a service and slot, pays a deposit or the full amount in test mode, receives an email, and both sides see the booking in their space | pending | — |
| 4 | Talk on the platform | Client and creative exchange messages about a booking without leaving the platform | pending | — |
| 5 | Reviews | A client whose booking is confirmed leaves a review shown on the creative's profile | pending | — |
| 6 | Production-ready beta | Security and GDPR checks passed, tested with clients and survey creatives, handover documentation complete | pending | — |

## Open Questions
- [ ] **Quotes:** does the « PROJET » slot (price on quote) exist, given the "no quotes" promise? — to confirm with the founders.
- [ ] **Booking confirmation:** is a booking confirmed automatically once paid, or does the creative accept it? This decides when reviews open (team decision: reviews open once the booking is confirmed, to confirm with the founders).
- [ ] **Success targets:** conversion and "regular clients" thresholds after launch.
- [ ] **Commission:** 5% charged to whom (client, creative, or split), and how does it combine with the freemium offer?
- [ ] **Beta testers:** how many clients and survey creatives will test the beta, and do the photo/video respondents suffice (most respondents are illustrators)?
- [ ] **Intellectual property:** the code currently belongs to the school; transfer terms to the founders are to be clarified.
- [ ] **Name:** "Uvision" vs "YouVision".

## Risks
| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Disintermediation: client and creative move off-platform after the first contact to avoid fees | High | High | Payment and messaging stay on the platform; low commission (5%); value only earned on-platform (reviews, future GDC points) |
| Empty results: France-wide and twelve categories spread few creatives thin, so many searches return nothing | High | High | Onboard survey respondents before opening to clients; search results that suggest nearby areas or related categories; track empty searches |
| No validated client demand ("book without a quote" is a founders' observation) | Medium | High | User tests with clients on the beta before production |
| Unfair reviews: reviews open once the booking is confirmed, before the session takes place | Medium | Medium | Confirm the rule; revisit when the validation code ships |
| Uneven quality with identity-only verification (successful platforms accept 2–30% of applicants) | Medium | Medium | Plan manual curation post-MVP |
| Survey sample does not represent creatives in the target (72% students, 46% illustrators) | High | Medium | Recruit photo/video creatives specifically for beta tests |
| Payment and identity data breach (GDPR) | Low | High | Delegate identity and card data to the payment provider; threat model and security tests before production |
| AI replacing some categories (products, real estate) | Medium | Low (MVP) | Watch category demand after launch |

---
*Status: DRAFT — requirements only. Implementation planning pending via /plan. Created 2026-11-23, revised 2026-11-23 (client focus, France-wide, all categories, reviews after confirmation).*
