# Uvision — Roadmap to the Showroom (6 April 2027)

Source of scope: [`PRD.md`](PRD.md). Roles: founders' kick-off email (section 3), plus design owned by Théodore.

Visual version (status, Gantt chart, per-person filter): [`docs/index.html`](docs/index.html), published at <https://theodoreroussard.github.io/uvision/> once GitHub Pages is enabled. This Markdown file stays the reference: update it first, then the HTML page.

## Assumptions

- **Sprints of two weeks**, Monday to Sunday. Every follow-up meeting falls in the first week of a sprint, so each meeting gets a demo of the sprint that just ended.
- **Capacity: 5 h per person per week**, 5 people, no lighter weeks, i.e. **25 h per week for the team, about 50 h per sprint, about 475 h in total**.
- **Deliverables are met on time.** If someone falls behind, the members who have completed their part of the sprint help them before taking on new work.
- **Each role owner builds the slice of their domain** and reviews the others' work in that domain (security, data, payments).
- **The client experience leads.** The creative storefront comes first only because the client journey needs creatives to find; every screen is judged by what it brings to the client.
- **Nothing is built yet** (23 November 2026).

## Timeline

| Sprint | Dates | Goal (PRD milestone) | School checkpoint | Demo at the checkpoint |
|---|---|---|---|---|
| S0 | 23/11 – 06/12 | Framing and foundations | Follow-up meeting 2 + peer assessment 1 (23–28/11) | PRD and roadmap |
| S1 | 07/12 – 20/12 | Creative storefront, part A (M1) | — | — |
| S2 | 21/12 – 03/01 | Creative storefront, part B (M1) | — | — |
| S3 | 04/01 – 17/01 | Find a creative (M2) | Follow-up meeting 3 + peer assessment 2 (04–09/01) | A creative publishes a storefront |
| S4 | 18/01 – 31/01 | Filters, book and pay, part A (M2, M3) | — | — |
| S5 | 01/02 – 14/02 | Book and pay, part B (M3) | Follow-up meeting 4 (01–06/02) | Search with filters, then booking and test payment |
| S6 | 15/02 – 28/02 | Messaging and reviews (M4, M5) | Follow-up meeting 5 (15–20/02, SSK hackathon week) | The full six-step journey |
| S7 | 01/03 – 14/03 | Hardening and user tests (M6) | Peer assessment 3 (08–13/03) | — |
| S8 | 15/03 – 28/03 | Release candidate, feature freeze (M6) | Follow-up meeting 6 (15–20/03) | Beta with messaging and reviews |
| S9 | 29/03 – 05/04 | Showroom and handover | Closing meeting (29/03 – 10/04) | Showroom on 06/04 |

## Sprints

### S0 — Framing and foundations (23/11 – 06/12)
Nothing user-visible yet. Every later sprint depends on these decisions.

| Who | Deliverable |
|---|---|
| Parikshit | Architecture diagram v1; data model v1 (users, profiles, services, availability, bookings, payments, reviews, portfolios, messages); dev, preview and production environments |
| Abdrahmane | Risk analysis v1; threat model v1; permissions matrix (client, creative, admin) |
| Maya | Data dictionary v1, aligned with the data model; key indicators (bookings, conversion, cancellations, retention); recruit photo and video beta testers from the survey |
| Alexandre | Repository scaffold (Next.js, TypeScript, Tailwind), CI, Better Auth wired in, i18n setup (French and English) |
| Théodore | Stripe Connect study and decision note; financial specification (booking statuses, deposit rules, 5% commission, refunds, payouts); design direction centred on the client journey: `impeccable init`, then `DESIGN.md` with AlignUI |

**Exit criteria:** the data model and permissions matrix are reviewed by the whole team; `DESIGN.md` exists.

### S1 — Creative storefront, part A (07/12 – 20/12)
| Who | Deliverable |
|---|---|
| Alexandre | Sign-up and sign-in screens; creative profile and portfolio pages |
| Parikshit | Schema and migrations for users, profiles and portfolios; image storage |
| Abdrahmane | Authentication hardening (password policy, sessions, account recovery); upload security (file type, size, metadata) |
| Théodore | Design of the creative onboarding and storefront screens (`impeccable shape`); services and prices data specification |
| Maya | French and English copy for these screens; seed data (fictional creatives across France, all twelve categories) |

### S2 — Creative storefront, part B (21/12 – 03/01)
| Who | Deliverable |
|---|---|
| Théodore | Services and prices API; deposit settings; creative payment account in Stripe test mode (light verification) |
| Alexandre | Services, prices and availability calendar screens |
| Parikshit | Availability and slot model |
| Abdrahmane | Ownership checks: a creative can only edit their own data; phone verification flow |
| Maya | Tracking plan: which events feed the key indicators |

**Milestone M1 done:** a creative signs up and publishes a storefront. Demo at follow-up meeting 3.

### S3 — Find a creative (04/01 – 17/01)
| Who | Deliverable |
|---|---|
| Alexandre | Search page, profile card, full profile |
| Parikshit | Search queries by category, budget, type, name, city and postcode across France; performance |
| Maya | Ranking criteria; definition of advanced filters (equipment, extra services, travel area); handling of empty results (nearby areas, related categories); recommendation study v1 |
| Théodore | Design of the search and profile screens; booking API contract |
| Abdrahmane | API security review (injections, rate limiting); what personal data a public profile exposes |

### S4 — Filters, book and pay, part A (18/01 – 31/01)
| Who | Deliverable |
|---|---|
| Alexandre | Advanced filters, including availability |
| Théodore | Booking API and statuses; deposit or full payment in Stripe test mode; 5% commission; automated tests of the financial rules |
| Parikshit | Bookings, payments and transaction history tables |
| Abdrahmane | Payment risk analysis; webhook signature checks; secrets and API key management |
| Maya | Key indicators dashboard specification |

**Milestone M2 done:** a client finds a creative with filters. Demo at follow-up meeting 4.

### S5 — Book and pay, part B (01/02 – 14/02)
| Who | Deliverable |
|---|---|
| Théodore | Idempotent webhooks; cancellation, refund, failed payment and pending payout cases; booking emails |
| Alexandre | Booking journey screens; client and creative personal spaces |
| Parikshit | Email service integration; staging environment |
| Abdrahmane | Authorisation tests on bookings (one user must never reach another's booking) |
| Maya | User test protocol; tester sessions scheduled for S7 |

**Milestone M3 done:** the full six-step journey works. Demo at follow-up meeting 5.

### S6 — Messaging and reviews (15/02 – 28/02)
| Who | Deliverable |
|---|---|
| Alexandre | Messaging screens |
| Parikshit | Message storage and delivery |
| Théodore | Reviews backend (open to clients whose booking is confirmed); notifications for messages |
| Abdrahmane | Abuse and moderation rules; detection of phone numbers and emails in messages; GDPR retention periods |
| Maya | Review indicators; French and English completeness check |

**Milestones M4 and M5 done.**

### S7 — Hardening and user tests (01/03 – 14/03)
| Who | Deliverable |
|---|---|
| Abdrahmane | Security tests; security report v1 |
| Maya | User tests with clients first, then survey creatives; findings summary |
| Théodore | `impeccable critique` and `audit` from Playwright screenshots (375, 768, 1440 px); fixes; financial flow documentation |
| Alexandre | Anomaly fixes; mobile and desktop checks; Playwright journey tests |
| Parikshit | Production environment, backups, monitoring |

### S8 — Release candidate (15/03 – 28/03)
Feature freeze: only fixes from the user tests and the security report.

| Who | Deliverable |
|---|---|
| Abdrahmane | Fix plan and incident plan; final security checklist |
| Parikshit | Final architecture and database documentation; installation and launch instructions |
| Théodore | API documentation; payment and financial flow documentation |
| Alexandre | Code documentation; list of known anomalies |
| Maya | Final data dictionary; data and AI roadmap; recommendations for the founders |

**Milestone M6 done:** a beta ready to go to production. Demo at follow-up meeting 6.

### S9 — Showroom and handover (29/03 – 05/04)
The handover pack from section 6 of the kick-off email, split by owner.

| Who | Deliverable |
|---|---|
| Parikshit | Installation instructions; access to the code and environments for the founders |
| Abdrahmane | Final security report and remaining risks |
| Maya | Showroom material; recommendations for what comes next |
| Alexandre | Demo script and demo data |
| Théodore | Feature status (done, incomplete, not started); roadmap for the next steps |

## Kick-off deliverables by owner

| Owner | Deliverable | Due |
|---|---|---|
| Parikshit | Architecture diagram | v1 S0, final S8 |
| Parikshit | Data model | v1 S0, final S8 |
| Parikshit | Technical documentation | S8 |
| Abdrahmane | Risk analysis and threat model | v1 S0, updated S4 (payments) |
| Abdrahmane | Permissions matrix | S0 |
| Abdrahmane | Security checklist | S8 |
| Abdrahmane | Test report | S7 |
| Maya | Data dictionary | v1 S0, final S8 |
| Maya | Key indicators | S0, dashboard spec S4 |
| Maya | Needs study | S7 (user tests) |
| Maya | Recommendation proposals | S3 |
| Maya | Data and AI roadmap | S8 |
| Alexandre | Working interfaces connected to the backend | S1 – S6 |
| Alexandre | Functional tests | S7 |
| Alexandre | Code documentation | S8 |
| Théodore | Business API | S2 – S6 |
| Théodore | Financial specification | S0 |
| Théodore | Test payment integration | S4 – S5 |
| Théodore | Flow documentation | S8 |
| Théodore | `DESIGN.md` and mockups | S0, then each sprint ahead of development |

## Risks to the plan

- **Mutual help.** When a member is late on a deliverable, members who have completed theirs help first; S8 (feature freeze) is the only buffer.
- **Théodore holds both design and payments.** The plan front-loads design (S0 – S3) and puts the payment work in S4 – S6. Design for later screens (messaging, personal spaces) must be ready one sprint ahead.
- **The SSK hackathon week (15–20/02)** falls in S6. If the hackathon takes the team's time, messaging slips to S7 and the user tests shrink.
- **Decisions still open in the PRD** (quotes, what confirms a booking and opens reviews, who pays the commission) must be settled with the founders by follow-up meeting 3 at the latest, before S4 starts.
