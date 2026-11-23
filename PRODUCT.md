# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Decided by the team:

- **Frontend:** Next.js + TypeScript + Tailwind CSS.
- **Database:** PostgreSQL (data model and setup by Parikshit).
- **Authentication:** Better Auth.
- **Deployment:** Vercel.
- **Payment:** Stripe Connect; clients pay on the platform (team decision, to confirm with the founders).

## Users

**Primary user (MVP): the individual client** who wants to book a photographer or videographer for a specific need (wedding, event, portrait, etc.), near them and within their budget. They arrive with a need, a location and a price range, and want to go from search to booking without waiting for a quote.

**Secondary user (MVP): the professional** (photographer, videographer, or both), including students, who wants to find clients, show their portfolio and manage their availability and bookings.

**Future audiences, outside the MVP:** companies (brands, agencies, SMEs, startups) that publish calls for tenders, and schools or academies teaching visual professions that manage their students.

## Product Purpose

Uvision is a platform for finding and booking visual professionals. The client chooses a creative, sees their availability and books a slot.

It exists because reaching a creative is slow and uncertain today: quotes, back-and-forth, waiting.

MVP success: one complete journey that can be tested end to end.

1. The client searches for a photographer or videographer.
2. They view the professional's profile and portfolio.
3. They pick a service and an available slot.
4. They make a booking.
5. They pay in a test environment.
6. They find their booking in their personal space.

## Positioning

Instant booking of a visual creative, without a quote, on a platform specialised in visual professions. The stated ambition is to create a booking standard for this fragmented market, as Planity and Doctolib did in their sectors.

What neighbours do not do: social networks give visibility without converting it into bookings; general freelance platforms are seen as complex and saturated.

## Operating Context

- Used on mobile and on desktop.
- Starting market: all of France, all twelve categories. International expansion is a longer-term ambition.
- In the MVP, the client searches by city or postcode. Geolocation and an interactive map of results come after the MVP.
- On the day of the session, client and professional are together on site: that is where the session is validated with a code (see below).
- The project is run by a student team for two cofounders; the result must be easy to take over after the team leaves (code, mockups, documentation).

## Capabilities and Constraints

### In the MVP

- **Search** by category, location, budget and type of professional; a professional can also be searched by name.
- **Categories:** Events, Sport, Corporate / Business, Fashion & Portrait, Real estate, Products / E-commerce, Lifestyle / Social media, Photobooth, Video / film production, Drone, Travel / nature, Technical / specialised.
- **Budget ranges:** under €100, €100–200, €200–500, €500 and over, custom amount.
- **Types of professional:** Photographer, Videographer, Photographer + Videographer.
- **Advanced filters**, visible after the first search: availability (immediate or on a date), rating and number of reviews, equipment (drone, 4K camera…), extra services (printed albums…), travel area.
- **Profile card** in the results: cover photo, name and rating, type of service, base price or package, availability, portfolio preview.
- **Full profile:** portfolio, biography, description, detailed prices, client reviews.
- **Reviews:** any client whose booking is confirmed can leave a review (team decision, to confirm with the founders).
- **Booking:** choice of service and date, online payment, confirmation by email, tracking in the personal space of both client and professional.
- **Messaging** between client and professional, on the platform.
- **Deposit**, at the professional's choice: can be turned on or off, fixed amount or percentage, limited to certain services, with refund conditions. The client clearly sees the amount due now, the balance and the due dates.
- **Sign-up and sign-in**, client and professional profiles, professional's calendar.

### Planned after the MVP

- **Validation code:** the client receives a unique code when booking and gives it to the professional at the end of the session; entering the code validates the session and releases the payment.
- **SMS confirmation** of bookings.
- **Graine de Champion (GDC):** points per shoot, 50 levels, five groups (Apprentis, Confirmés, Experts, Élite, Champions), national and international rankings, badges, yearly rewards.
- **Uvision Award:** photo and video competition twice a year, for professionals only, with voting by registered users.
- **Uvision Ads:** carousel advertising slots for brands, on the home page, the search page and the professional dashboard.
- **Company and School accounts**, calls for tenders and casting.
- Favourites, FAQ, blog, partners page, « le saviez-vous » (did you know), yearly recap, comparison of professionals, link to a Behance portfolio, promo codes, temporary account deactivation.
- Extension to other visual professions: graphic designers, video editors, motion designers, illustrators, retouchers, content creators.
- Recommendations by artificial intelligence.

### Constraints

- **Professional verification:** light in the MVP (verified phone, identity check through the payment provider). The full target, after the MVP: identity document, status (SIRET number, optional for students), IBAN, two-factor authentication.
- **GDPR** and data protection, especially identity documents and payment data.
- **Payment** through Stripe Connect, a marketplace-type solution.

- **Interface languages:** French and English (team decision). Every screen must work in both, including longer French strings. Which language is shown by default is not defined.

### Working assumptions

Adopted by the team to move forward, to be confirmed by the founders because the source documents contradict each other on these points.

- **Payment flow:** the client pays on the platform, not directly to the professional.
- **Revenue model:** freemium for professionals, plus a 5% commission on bookings. What the free and paid offers contain, and who pays the commission (client, professional or both), are not defined. The yearly fees in the specification (€24/year for students, €48/year for professionals) are not carried over as they stand.

### Open decisions

The source documents contradict each other or are incomplete on these points. Invent nothing: ask before designing a screen that depends on one of them.

- **Quotes:** the promise is "no quotes", but a « PROJET » (project) slot in the calendar allows prices on quote (music videos, shoots abroad).
- **Name:** "Uvision" everywhere, "YouVision" mentioned once.
- **Booking confirmation:** confirmed automatically once paid, or after the professional accepts? This decides when reviews open.
- **GDC:** the role of speed in the score, the benefits attached to rewards ("to be defined"), and the level rule (levels are said never to reset to zero, yet the career score can go down).
## Brand Commitments

- **Name:** Uvision.
- **Slogan:** « Réservez * Créez * Brillez » (Book, Create, Shine). The slogan exists in French only.
- **Positioning line:** « Simple. Rapide. Instantané. » (Simple. Fast. Instant.) In French only.
- **Colours:** blue, purple, grey and white are the founders' initial orientation, explicitly not binding.
- **Creative freedom:** there is no logo, mascot, brand guidelines or mockup. The founders deliberately leave the team free to propose its vision; logo, mascot and guidelines are among the directions to explore.

## Evidence on Hand

- `ESILV PROJET UVISION.pdf`: functional specification (19 pages).
- `ESILV SUMMARY UVISION.pdf`: executive summary (team, project, advantages, customers).
- `Re- Project Kick-off.pdf`: the founders' kick-off email (vision, priorities, deliverables).
- `ÉTUDE-Créateurs-visuels-️.pdf`: survey of 50 visual creatives (November 2026), summarised in `PRD.md`.
- `PRD.md`: MVP requirements; `ROADMAP.md`: sprint plan to the showroom on 6 April 2027.

Gaps that must not be filled with invention: no logo, no portfolio photos or videos, no real registered professional, no review or testimonial, no client-side data, no usage figures, no confirmed partnership with a brand or school (Canon, Sony, etc. are named as advertising targets, not as partners).

## Product Principles

1. **From search to booking without waiting.** Any step that feels like a quote request or a back-and-forth is a product failure.
2. **The professional's work is the proof.** Portfolio, reviews and price carry the client's decision.
3. **Money is always readable.** Price, deposit, balance and refund conditions are visible before committing.
4. **Trust is protected on both sides.** Verified professionals for the client, guaranteed payment for the professional.
5. **A complete journey before extra features.** The MVP comes before gamification, advertising and competitions.
