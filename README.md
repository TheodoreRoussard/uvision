# Uvision

**Réservez · Créez · Brillez** (Book · Create · Shine)

Uvision is a web platform for finding and booking visual professionals. A client finds a photographer or videographer that matches their need, location and budget, looks at their portfolio, sees their availability and books a slot, without going through a quote.

## What the app does

### First version (MVP)

The goal is one complete journey that can be tested end to end:

(1) Direct choice
1. The client searches for a photographer or videographer.
2. They view the professional's profile and portfolio.
3. They pick a service and an available slot.
4. They make a booking.
5. They pay in a test environment.
6. They find their booking in their personal space.

(2) Announcements (after the MVP, sprint S8; kept by the founders next to direct choice)
1. The client post their needs and conditions
2. The post appear on the professionals feed (based on the filters and the photography categories, e.g availability)
3. The professional choose which post they want to attend
4. Payment transfered when the service is booked (to see)
5. They find their booking in their personal space.
Features covered:

- **Search** by category (wedding, events, corporate, real estate, drone…), by city or postcode (map and geolocation after the MVP), by budget and by type of professional.
- **Advanced filters:** availability, rating and number of reviews, experienced (completed bookings on Uvision), equipment, extra services, travel area.
- **Professional profiles:** portfolio, biography, services and prices, client reviews, link or preview of a Behance page or website.
- **Online booking** with an availability calendar and confirmation by email (SMS after the MVP).
- **Messaging** between client and professional (primordial for the founders).
- **Payment on the platform** through Stripe, with an optional deposit set by the professional.
- **Personal spaces** for the client and for the professional.

### After the MVP, by the showroom (6 April 2027)

- Session validation code, which releases the professional's payment.
- SMS confirmation, full verification, map and geolocation.
- Announcements: the client posts a need, professionals apply.
- Graine de Champion: points, levels, rankings and badges for professionals.
- Uvision Award: photo and video competition.
- Company and School accounts, calls for tenders.
- Extension to other visual professions (graphic designers, video editors, motion designers…).

### Business model

Confirmed by the founders: a fixed commission on bookings, deducted from the professional's payout, next to a freemium offer whose content is still to define. Uvision Ads is set aside for a future version.

**Commissions :** 
- 5% for professionals
- 2% for students from partner schools (proved by a school email address)

## Tech stack

| Layer | Choice |
|---|---|
| Frontend | [Next.js](https://nextjs.org) + TypeScript + [Tailwind CSS](https://tailwindcss.com) |
| Database | [PostgreSQL](https://www.postgresql.org) |
| Authentication | [Better Auth](https://www.better-auth.com) |
| Deployment | [Vercel](https://vercel.com) |
| Payment | Stripe Connect |

## Project status

The project is just starting: this repository contains no code yet. Installation and run instructions will be added with the first version of the app.

## Repository documentation

- [`PRODUCT.md`](PRODUCT.md): product context (users, scope, constraints, open decisions).
- [`CLAUDE.md`](CLAUDE.md): working rules for designing and verifying the interface.

## Team

Project carried out by a team of ESILV students for the cofounders of Uvision.
