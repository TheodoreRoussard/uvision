# Product

<!-- impeccable:product-schema 1 -->

Design-oriented context for the interface. Scope, business rules and open questions live in `PRD.md`; the sprint plan lives in `ROADMAP.md`. This file does not repeat them.

## Platform

web

## Stack

Decided by the team:

- **Frontend:** Next.js + TypeScript + Tailwind CSS.
- **Database:** PostgreSQL (data model and setup by Parikshit).
- **Authentication:** Better Auth.
- **Deployment:** Vercel.
- **Payment:** Stripe Connect.

## Users

**The individual client** arrives with a need (wedding, event, portrait…), a place and a price range, often on a phone, and wants to reach a booking without asking for a quote. They book in one of two ways: by choosing a creative from their profile and portfolio, or (after the MVP) by publishing their need as an announcement and picking among the creatives who apply.

**The creative** (photographer, videographer or both, often a student) manages a storefront: portfolio, priced services, calendar, deposit settings, bookings and messages. They work from desktop as much as from mobile.

Who they are and why they need Uvision: see `PRD.md` (Users, Evidence).

## Product Purpose

Uvision is a platform for finding and booking visual professionals. The client chooses a creative, sees their availability and books a slot.

It exists because reaching a creative is slow and uncertain today: quotes, back-and-forth, waiting.

The MVP (14 February 2027) is one complete journey, tested end to end:

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
- All of France, all twelve categories from day one.
- In the MVP, the client searches by city or postcode. A map of results comes later.
- On the day of the session, client and creative are together on site: that is where the session is validated with a code (after the MVP).
- The team stops after the showroom on 6 April 2027 and the founders take over: designs, components and documentation must be easy to pick up.

## Capabilities and Constraints

The interface has to hold these screens and features; their exact content is in `PRD.md` (Scope).

- **MVP:** search with advanced filters, result cards, full profile with portfolio, booking of a service and slot, payment with deposit, personal space for client and creative, messaging, reviews, sign-up and creative storefront.
- **By the showroom:** validation code, map, full verification, Graine de Champion levels and rankings, Uvision Award, announcements, company and school accounts, secondary pages.

Design constraints:

- **Two languages:** every screen works in French and English, including longer French strings. The default language is not decided.
- **Money on screen:** price, deposit, balance, due dates and refund conditions are shown before the user commits.
- **Sensitive data:** identity documents and payment details are handled by the payment provider; screens never ask for more than they need.
- **Open questions:** several screens depend on undecided rules (quotes, booking confirmation, announcement pricing, experienced filter, GDC rules). Check `PRD.md` (Open Questions) and ask before designing one of them; invent nothing.

## Brand Commitments

- **Name:** Uvision.
- **Slogan:** « Réservez * Créez * Brillez » (Book, Create, Shine). The slogan exists in French only.
- **Positioning line:** « Simple. Rapide. Instantané. » (Simple. Fast. Instant.) In French only.
- **Colours:** blue, purple, grey and white are the founders' initial orientation, explicitly not binding.
- **Creative freedom:** there is no logo, mascot, brand guidelines or mockup. The founders deliberately leave the team free to propose its vision; logo, mascot and guidelines are among the directions to explore.

## Evidence on Hand

Sources and research are listed in `PRD.md` (Evidence).

Gaps that must not be filled with invention in designs: no logo, no portfolio photos or videos, no real registered creative, no review or testimonial, no usage figures, no confirmed partnership with a brand or school. Use clearly marked placeholders instead.

## Product Principles

1. **From search to booking without waiting.** Any step that feels like a quote request or a back-and-forth is a product failure.
2. **The professional's work is the proof.** Portfolio, reviews and price carry the client's decision.
3. **Money is always readable.** Price, deposit, balance and refund conditions are visible before committing.
4. **Trust is protected on both sides.** Verified professionals for the client, guaranteed payment for the professional.
5. **A complete journey before extra features.** The MVP comes before gamification, competitions and announcements.
