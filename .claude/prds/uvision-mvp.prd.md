# Uvision — MVP and Showroom Release

## Problem
People in France who need a photographer or videographer for a specific occasion (event, portrait, corporate shoot) find it slow and uncertain to hire one: they browse social networks or directories, ask for quotes, wait for answers and go back and forth before knowing the price or whether the creative is free. Meanwhile, emerging creatives, many of them students, struggle to be seen and to turn their work into paid bookings. Left unsolved, clients give up or settle for the first available option, and good creatives stay invisible.

## Evidence
- **Client side:** founders' observation — "reaching a creative remains complex, slow and uncertain". Assumption — needs validation via user testing with clients on the beta.
- **Creative survey, 50 respondents (Nov. 2026):** 69% cite lack of visibility as their main problem, 57% finding clients; 58% have no client yet; 69% do not find clients easily (36 answers); 66% use no platform, and those who do mostly use Instagram. Sample bias: 72% students, 46% illustration — only part of it is photo/video.
- **Respondent quote:** "Job search platforms are too poorly suited to artists."
- **Commission tolerance (survey):** 8% acceptable for 47%, 10% for 22%, 5% for 20%.
- **Launch interest (survey):** 92% want to be told when the platform opens.
- **Platforms creatives use today (team, first founders' meeting, 17 Nov. 2026):** Instagram, TikTok, LinkedIn, Vgen (too restrictive, needs a patronage system), Shootday (events in Paris and Cannes only), and lesser-known generalist platforms.
- **Practitioner feedback:** the team tried to contact a professional photographer for their opinion (Nov. 2026); no feedback recorded yet. The founders asked which photographer was contacted and what was learned.
- **Market (secondary analysis, sources not independently verified):** no French equivalent for consumers with on-platform booking and payment — only directories (Mariages.net, PhotoPresta) and B2B services (Utopix, Shoootin); Meero was ~95% B2B. Comparable models abroad: Snappr (closest), Lovegraph (Japan), SweetEscape, Flytographer, Perfocal. "64% of French couples find their suppliers on a specialised site or app" — single figure, source to confirm.
- **"Market not yet exploited in France":** Assumption — needs validation via market sizing (number of independent visual creatives, booking volume).

## Users
- **Primary**: the individual client in France with a one-off need (wedding, event, portrait, corporate, product…), a location and a budget, who wants to go from search to a paid booking without asking for a quote or waiting for an answer.
- **Secondary**: the visual creative — photographer, videographer or both, often a student or early-career independent — who needs to be found, show a portfolio, sell fixed-price services and get paid. Their storefront is what makes the client journey possible.
- **Later in the project (after the MVP, before the showroom)**: companies and brands (calls for tenders, casting), schools, creatives outside photo/video.

## Hypothesis
We believe **instant booking of a photographer or videographer — with portfolio, fixed prices, real availability and on-platform payment visible upfront** — will **remove the quote-and-wait friction of hiring a visual creative** for **individual clients in France**.
We'll know we're right when **clients who search go on to book and pay without contacting the creative first**, and **creatives get regular clients through the platform** (targets TBD — see Open Questions).

## Success Metrics
Project success (6 April 2027) is **the whole specification built, tested and ready for production**, handed over to the founders, who launch it themselves: the team stops working on the project after the showroom. The MVP, finished on 14 February 2027, proves the core journey first. Product success is measured after launch.

| Metric | Target | How measured |
|---|---|---|
| End-to-end client journey works (search → profile → service and slot → booking → test payment → personal space) | 100% of steps pass | Automated end-to-end tests in a test environment |
| Client usability | TBD — share of test clients who complete a booking without help | Moderated user tests on the beta |
| Creative side ready to receive bookings (sign-up → storefront → booking received) | 100% of steps pass | Automated end-to-end tests |
| Specification coverage at the showroom | 100% of the specification's features built and tested; anything unfinished at the feature freeze (28 March) is specified and documented | Feature status against the specification |
| Production readiness | Security checklist and GDPR review passed, no open critical vulnerability; go-live procedure documented for the founders (live payment keys, domain, environments) | Security test report; go-live checklist |
| Handover readiness | All end-of-project deliverables from the kick-off email present | Checklist review with the founders |
| *(post-launch)* Search-to-booking conversion | TBD | Booking analytics |
| *(post-launch)* Regular clients for creatives | TBD — e.g. share of creatives with ≥ N bookings per month | Booking analytics |

## Scope
**MVP — by 14 February 2027 (end of S5)** — A version that a client and a creative can use end to end in a test payment environment, across **all of France** and **all twelve categories** (Events, Sport, Corporate / Business, Fashion & Portrait, Real estate, Products / E-commerce, Lifestyle / Social media, Photobooth, Video / film production, Drone, Travel / nature, Technical / specialised):
- Client side: search by category, location (city or postcode), budget, type of professional and name; **advanced filters** (availability, rating and reviews, **experienced** — at least N bookings completed on Uvision, N to set — equipment, extra services, travel area); profile card and full profile; booking of a service and slot; payment on the platform (deposit or full amount, with balance and due dates shown upfront); email confirmation; booking tracking in a personal space; **reviews**, open to any client whose booking is confirmed.
- Creative side: sign-up and sign-in, light verification (phone, identity check through the payment provider in test mode), student status through a partner school email address, profile, portfolio, link or preview of a Behance page or personal site (there is no Behance API), services with fixed prices, availability calendar, configurable deposit (on/off, fixed or percentage, per service, refund conditions), booking tracking in a personal space.
- Both: **in-platform messaging** between client and creative — "primordial" for the founders.
- Interface in French and English.
- Payment through Stripe, connected to Uvision (Stripe Connect; confirmed by the founders).
- Commission, fixed and deducted from the creative's payout: **5%** for professionals, **2%** for students of partner schools. Experience shows in the creative's base price, not in the rate.

**Showroom release — by 6 April 2027 (feature freeze 28 March)** — the rest of the specification, built on top of the MVP:
- Trust and session: validation code given at the end of the session that releases the payment; SMS confirmation; full creative verification (identity document, SIRET number, optional for students, IBAN, two-factor authentication); interactive map of results and geolocation.
- Community: Graine de Champion (points per shoot, 50 levels, five groups, national and international rankings, badges, yearly rewards); Uvision Award (photo and video competition, voting by registered users).
- Other segments: Company and School accounts, calls for tenders, casting.
- **Announcements**, the second way to book, kept by the founders next to direct choice: the client publishes a need as an announcement, the matching creatives see it in their feed and apply, and the client picks one.
- Growth: promo codes; AI recommendations; extension to other visual professions (graphic designers, video editors, motion designers, illustrators, retouchers, content creators).
- Secondary features: favourites, FAQ, blog, partners page, « le saviez-vous », yearly recap, comparison of creatives, temporary account deactivation.

**Out of scope**
- Going live (live payment keys, domain, first real users) — done by the founders after the showroom, from the team's go-live procedure.
- Uvision Ads — set aside by the founders for a future version: ads would hurt a professional platform's credibility and earn little (about €150 for 30,000 views against about €12.50 net per €150 booking).
- Logo or mascot contest — an idea for the official launch.
- International launch — a longer-term ambition of the founders.
- Manual quality curation of creatives — not in the specification; see Risks.

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
| 6 | MVP complete (14 Feb.) | The six-step journey, messaging and reviews pass end-to-end tests and a first round of user tests | pending | — |
| 7 | Trust and session | The validation code releases the payment, bookings are confirmed by SMS, creatives pass full verification, clients search on a map | pending | — |
| 8 | Community and businesses | Creatives earn Graine de Champion points and levels, enter the Uvision Award, and companies and schools publish calls for tenders | pending | — |
| 9 | Announcements, AI and extras | A client publishes a need and books one of the creatives who applied; clients get AI recommendations; other visual professions can sign up; secondary features are in place | pending | — |
| 10 | Ready for launch (6 Apr.) | Security and GDPR checks passed, handover pack and go-live procedure delivered to the founders | pending | — |

## Open Questions
- [ ] **Quotes:** does the « PROJET » slot (price on quote) exist, given the "no quotes" promise? — to confirm with the founders.
- [ ] **Booking confirmation:** is a booking confirmed automatically once paid, or does the creative accept it? This decides when reviews open (team decision: reviews open once the booking is confirmed, to confirm with the founders).
- [ ] **Success targets:** conversion and "regular clients" thresholds after launch.
- [x] **Commission:** fixed, deducted from the creative's payout — 5% for professionals, 2% for students of partner schools (founders, Nov. 2026).
- [ ] **Partner schools:** which schools, and which email domains prove a student's status?
- [ ] **Freemium:** what the free and paid creative offers contain, next to the commission.
- [ ] **"Experienced" filter:** the team proposes at least N bookings completed on Uvision; which N? The filter is empty at launch, when nobody has bookings yet.
- [ ] **Announcements:** do creatives apply with their listed services and prices, or with a custom price? A custom price comes close to the quote the product promises to remove.
- [ ] **Beta testers:** how many clients and survey creatives will test the beta, and do the photo/video respondents suffice (most respondents are illustrators)?
- [ ] **Intellectual property:** the code currently belongs to the school; transfer terms to the founders are to be clarified.
- [ ] **Name:** "Uvision" vs "YouVision".
- [ ] **Validation code and payment release:** photos are delivered after the session; is the payment released when the code is entered, or when the photos are delivered?
- [ ] **Graine de Champion rules:** the role of speed in the score, the benefits attached to rewards, and how levels "never reset" while the career score can go down — needed before S7.

## Risks
| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Disintermediation: client and creative move off-platform after the first contact to avoid fees | High | High | Payment and messaging stay on the platform; low commission (5%, 2% for students); value only earned on-platform (reviews, future GDC points) |
| Empty results: France-wide and twelve categories spread few creatives thin, so many searches return nothing | High | High | Onboard survey respondents before opening to clients; search results that suggest nearby areas or related categories; track empty searches |
| No validated client demand ("book without a quote" is a founders' observation) | Medium | High | User tests with clients on the beta before production |
| Unfair reviews: reviews open once the booking is confirmed, before the session takes place | Medium | Medium | Confirm the rule; revisit when the validation code ships |
| Uneven quality with identity-only verification (successful platforms accept 2–30% of applicants) | Medium | Medium | Plan manual curation post-MVP |
| Survey sample does not represent creatives in the target (72% students, 46% illustrators) | High | Medium | Recruit photo/video creatives specifically for beta tests |
| Payment and identity data breach (GDPR) | Low | High | Delegate identity and card data to the payment provider; threat model and security tests before production |
| AI replacing some categories (products, real estate) | Medium | Low (MVP) | Watch category demand after launch |
| Scope: the whole specification in about 760 h; the post-MVP modules get three sprints and no buffer | High | High | Build in priority order (trust and session, community, businesses, ads, AI, extras); feature freeze on 28 March; anything unfinished is delivered specified and documented |
| No one maintains the platform after the showroom | High | Medium | Handover pack, go-live procedure and known-issues list written for whoever the founders hire |

---
*Status: DRAFT — requirements only. Implementation planning pending via /plan. Created 2026-11-23, revised 2026-11-23 (client focus, France-wide, all categories, reviews after confirmation), revised 2026-11-26 (MVP by 14 February; whole specification by the showroom; 8 h per person per week; founders go live), revised 2026-11-26 (founders' answers to the first meeting: commission 5% / 2%, Stripe, announcements kept, Ads set aside, experienced filter, Behance link).*
