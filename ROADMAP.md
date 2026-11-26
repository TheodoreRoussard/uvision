# Uvision — Roadmap to the Showroom (6 April 2027)

Source of scope: [`PRD.md`](PRD.md). Roles: founders' kick-off email (section 3), plus design owned by Théodore.

Visual version (status, Gantt chart, per-person filter): [`docs/index.html`](docs/index.html), published at <https://theodoreroussard.github.io/uvision/> once GitHub Pages is enabled. This Markdown file stays the reference: update it first, then the HTML page.

## Assumptions

- **The whole specification is built by the showroom.** The team stops working on the project on 6 April 2027. Nothing is planned after that date: the founders launch the platform themselves from the handover pack.
- **The MVP comes first, by 14 February** (end of S5): the six-step journey, messaging and reviews. Sprints S6 to S8 build everything else in the specification.
- **Sprints of two weeks**, Monday to Sunday. Every follow-up meeting falls in the first week of a sprint, so each meeting gets a demo of the sprint that just ended.
- **Capacity: 8 h per person per week**, 5 people, no lighter weeks, i.e. **40 h per week for the team, about 80 h per sprint, about 760 h in total**.
- **Deliverables are met on time.** If someone falls behind, the members who have completed their part of the sprint help them before taking on new work.
- **Each role owner builds the slice of their domain** and reviews the others' work in that domain (security, data, payments).
- **The client experience leads.** The creative storefront comes first only because the client journey needs creatives to find; every screen is judged by what it brings to the client.
- **Post-MVP modules are built in priority order:** trust and session, then community, then companies and schools, then announcements, AI and secondary features. Anything unfinished at the feature freeze (28 March) is delivered specified and documented.
- **Nothing is built yet** (23 November 2026).

## Timeline

| Sprint | Dates | Goal (PRD milestone) | School checkpoint | Demo at the checkpoint |
|---|---|---|---|---|
| S0 | 23/11 – 06/12 | Framing and foundations | Follow-up meeting 2 + peer assessment 1 (23–28/11) | PRD and roadmap |
| S1 | 07/12 – 20/12 | Creative storefront (M1) | — | — |
| S2 | 21/12 – 03/01 | Find a creative (M2) | — | — |
| S3 | 04/01 – 17/01 | Book and pay (M3) | Follow-up meeting 3 + peer assessment 2 (04–09/01) | A creative publishes a storefront; search with filters |
| S4 | 18/01 – 31/01 | Messaging and reviews (M4, M5) | — | — |
| S5 | 01/02 – 14/02 | MVP complete (M6) | Follow-up meeting 4 (01–06/02) | Booking and test payment, messaging, reviews |
| S6 | 15/02 – 28/02 | Trust and session (M7) | Follow-up meeting 5 (15–20/02, SSK hackathon week) | The complete MVP, tested end to end |
| S7 | 01/03 – 14/03 | Community and businesses (M8) | Peer assessment 3 (08–13/03) | — |
| S8 | 15/03 – 28/03 | Announcements, AI and extras (M9), feature freeze on 28/03 | Follow-up meeting 6 (15–20/03) | Validation code, verification, map, Graine de Champion, Award, company and school accounts |
| S9 | 29/03 – 05/04 | Stabilisation and handover (M10) | Closing meeting (29/03 – 10/04) | Showroom on 06/04: the whole specification |

## Sprints

### S0 — Framing and foundations (23/11 – 06/12)
Nothing user-visible yet. Every later sprint depends on these decisions.

| Who | Deliverable |
|---|---|
| Parikshit | Architecture diagram v1; data model v1 for the MVP (users, profiles, services, availability, bookings, payments, reviews, portfolios, messages), designed to take the post-MVP modules; dev, preview and production environments |
| Abdrahmane | Risk analysis v1; threat model v1; permissions matrix (client, creative, admin, then company and school) |
| Maya | Data dictionary v1, aligned with the data model; key indicators (bookings, conversion, cancellations, retention); recruit photo and video beta testers from the survey |
| Alexandre | Repository scaffold (Next.js, TypeScript, Tailwind), CI, Better Auth wired in, i18n setup (French and English) |
| Théodore | Progress tracking on GitHub for the founders (repository created; milestones M1 – M10, one issue per deliverable, kept up to date each sprint); Stripe Connect study and decision note; financial specification (booking statuses, deposit rules, commission of 5% or 2% for partner-school students deducted from the payout, refunds, payouts, validation code); design direction centred on the client journey: `impeccable init`, then `DESIGN.md` with AlignUI |

**Exit criteria:** the data model and permissions matrix are reviewed by the whole team; `DESIGN.md` exists.

### S1 — Creative storefront (07/12 – 20/12)
| Who | Deliverable |
|---|---|
| Alexandre | Sign-up and sign-in screens; creative profile, portfolio, services and prices screens; link and preview of a Behance page or website; availability calendar |
| Parikshit | Schema and migrations for users, profiles, portfolios, services and availability; image storage |
| Abdrahmane | Authentication hardening (password policy, sessions, account recovery); upload security; ownership checks; phone verification flow; student status through a partner school email address |
| Théodore | Design of the onboarding, storefront and search screens (`impeccable shape`); services and prices API; deposit settings; creative payment account in Stripe test mode |
| Maya | French and English copy for these screens; seed data (fictional creatives across France, all twelve categories); tracking plan |

**Milestone M1 done:** a creative signs up and publishes a storefront.

### S2 — Find a creative (21/12 – 03/01)
| Who | Deliverable |
|---|---|
| Alexandre | Search page, profile card, full profile; advanced filters, including availability and « experienced » |
| Parikshit | Search queries by category, budget, type, name, city and postcode across France, with the filters; performance |
| Maya | Ranking criteria; definition of the advanced filters, including the « experienced » threshold (completed bookings); handling of empty results (nearby areas, related categories); recommendation study v1 |
| Théodore | Design of the booking, personal space and messaging screens; booking API contract |
| Abdrahmane | API security review (injections, rate limiting); what personal data a public profile exposes |

**Milestone M2 done:** a client finds a creative with filters. Demo at follow-up meeting 3, with M1.

### S3 — Book and pay (04/01 – 17/01)
| Who | Deliverable |
|---|---|
| Théodore | Booking API and statuses; deposit or full payment in Stripe test mode; commission (5%, or 2% for partner-school students) deducted from the creative's payout; idempotent webhooks; cancellation and refund cases; automated tests of the financial rules |
| Alexandre | Booking journey screens; client and creative personal spaces |
| Parikshit | Bookings, payments and transaction history tables; email service integration |
| Abdrahmane | Payment risk analysis; webhook signature checks; secrets management; authorisation tests on bookings (one user must never reach another's booking) |
| Maya | Key indicators dashboard specification; user test protocol |

**Milestone M3 done:** a client books and pays in test mode; both sides see the booking.

### S4 — Messaging and reviews (18/01 – 31/01)
| Who | Deliverable |
|---|---|
| Alexandre | Messaging screens; review screens |
| Parikshit | Message storage and delivery; notifications |
| Théodore | Reviews backend (open to clients whose booking is confirmed); booking emails; design of the trust and session screens (validation code, verification, map) |
| Abdrahmane | Abuse and moderation rules; detection of phone numbers and emails in messages; GDPR retention periods |
| Maya | Review indicators; Graine de Champion rules specification (points, levels, groups, rankings, badges) for the founders to validate |

**Milestones M4 and M5 done.**

### S5 — MVP complete (01/02 – 14/02)
| Who | Deliverable |
|---|---|
| Alexandre | Playwright end-to-end tests of the MVP journeys; mobile and desktop fixes |
| Théodore | `impeccable critique` and `audit` of the MVP (375, 768, 1440 px) and fixes; failed payment and pending payout cases; validation code and payment release specification |
| Parikshit | Staging environment; data model v2 for the post-MVP modules (validation code, verification, Graine de Champion, Award, company and school accounts, announcements) |
| Abdrahmane | MVP security tests; security report v1; full verification specification (identity document, SIRET, IBAN, two-factor authentication) |
| Maya | MVP user tests with clients and survey creatives; Award rules and announcement matching rules |

**Milestone M6 done:** the MVP is complete. Demo at follow-up meeting 5.

### S6 — Trust and session (15/02 – 28/02)
| Who | Deliverable |
|---|---|
| Théodore | Validation code that releases the payment; SMS confirmation of bookings |
| Alexandre | Interactive map of results and geolocation; validation code screens |
| Parikshit | Geolocation queries; SMS provider integration |
| Abdrahmane | Full verification (identity document through the payment provider, SIRET, IBAN); two-factor authentication |
| Maya | User test findings and fixes list; content for the FAQ, « le saviez-vous » and partners page |

**Milestone M7 done.**

### S7 — Community and businesses (01/03 – 14/03)
| Who | Deliverable |
|---|---|
| Théodore | Graine de Champion engine (points, levels, groups, rankings, badges, yearly rewards); billing rules for company and school accounts; design of the announcement screens |
| Alexandre | Graine de Champion and Uvision Award screens (submission, voting); company and school account screens |
| Parikshit | Calls for tenders and casting backend; Award voting backend |
| Abdrahmane | Vote fraud prevention; permissions for company and school accounts; security tests of the new modules |
| Maya | Rankings and yearly recap indicators; key indicators dashboard |

**Milestone M8 done.**

### S8 — Announcements, AI and extras (15/03 – 28/03)
Feature freeze on 28/03: after that date, only fixes. Uvision Ads is set aside by the founders for a future version; announcements take its place.

| Who | Deliverable |
|---|---|
| Théodore | Announcements backend: a client publishes a need, creatives apply, the client picks one, booking and payment follow; promo codes |
| Alexandre | Announcement screens (publish a need, creatives' feed, applications); favourites, FAQ, blog, partners page, « le saviez-vous », comparison of creatives, temporary account deactivation |
| Parikshit | Matching announcements to creatives (category, area, availability); extension to other visual professions; final architecture and database documentation |
| Maya | AI recommendations v1; final data dictionary; data and AI roadmap for the founders |
| Abdrahmane | Security of announcements (spam, contact details); final security tests; incident plan; final security checklist |

**Milestone M9 done.** Demo of M7 and M8 at follow-up meeting 6.

### S9 — Stabilisation and handover (29/03 – 05/04)
The handover pack from section 6 of the kick-off email, split by owner. Nobody works on the project after the showroom, so the pack must let the founders launch and maintain the platform without the team.

| Who | Deliverable |
|---|---|
| Parikshit | Installation instructions; go-live procedure (live payment keys, domain, environments); access to the code and environments for the founders |
| Abdrahmane | Final security report and remaining risks |
| Maya | Showroom material; recommendations for the founders |
| Alexandre | Demo script and demo data; code documentation; list of known anomalies |
| Théodore | Feature status against the specification (done, specified only); API and financial flow documentation |

**Milestone M10 done:** the platform is ready for the founders to launch. Showroom on 06/04.

## Kick-off deliverables by owner

| Owner | Deliverable | Due |
|---|---|---|
| Parikshit | Architecture diagram | v1 S0, final S8 |
| Parikshit | Data model | v1 S0, v2 S5, final S8 |
| Parikshit | Technical documentation and go-live procedure | S8 – S9 |
| Abdrahmane | Risk analysis and threat model | v1 S0, updated S3 (payments) and S5 (verification) |
| Abdrahmane | Permissions matrix | S0, extended S7 |
| Abdrahmane | Security checklist | S8 |
| Abdrahmane | Test report | v1 S5, final S9 |
| Maya | Data dictionary | v1 S0, final S8 |
| Maya | Key indicators | S0, dashboard spec S3, dashboard S7 |
| Maya | Needs study | S5 (user tests) |
| Maya | Recommendation proposals | S2, AI recommendations S8 |
| Maya | Data and AI roadmap | S8 |
| Alexandre | Working interfaces connected to the backend | S1 – S8 |
| Alexandre | Functional tests | S5, then each sprint |
| Alexandre | Code documentation | S9 |
| Théodore | Progress tracking on GitHub | S0, then each sprint |
| Théodore | Business API | S1 – S8 |
| Théodore | Financial specification | S0 |
| Théodore | Test payment integration | S3 – S5 |
| Théodore | Flow documentation | S9 |
| Théodore | `DESIGN.md` and mockups | S0, then each sprint ahead of development |

## Risks to the plan

- **The whole specification in about 760 h.** The post-MVP modules get three sprints and no buffer. They are built in priority order; anything unfinished at the feature freeze is delivered specified and documented, and listed in the feature status.
- **No buffer before the showroom.** The S8 freeze is followed by a one-week S9 for fixes and handover only. Mutual help comes first when a member is late.
- **Nobody maintains the platform after 6 April.** The founders launch it from the handover pack, so documentation is a deliverable, not an afterthought.
- **Théodore holds both design and payments.** Design is front-loaded (S0 – S2) and stays one sprint ahead of development; payment work sits in S3 – S6.
- **The SSK hackathon week (15–20/02)** falls in S6. If the hackathon takes the team's time, the trust and session work slips into S7 and pushes the lowest-priority extras out of S8.
- **Decisions still open in the PRD** must be settled with the founders before the work that depends on them: the « experienced » threshold before S2 starts (21 December); quotes, what confirms a booking and opens reviews, and the list of partner schools before S3 starts (4 January); payment release with the validation code before S6 (15 February); Graine de Champion rules before S7 (1 March); whether announcements take listed or custom prices before S8 (15 March).
