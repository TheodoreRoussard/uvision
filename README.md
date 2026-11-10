# Uvision

**Réservez · Créez · Brillez** (Book · Create · Shine)

Uvision is a web platform for finding and booking visual professionals. A client finds a photographer or videographer that matches their need, location and budget, looks at their portfolio, sees their availability and books a slot, without going through a quote.

## What the app does

### First version (MVP)

The goal is one complete journey that can be tested end to end:

1. The client searches for a photographer or videographer.
2. They view the professional's profile and portfolio.
3. They pick a service and an available slot.
4. They make a booking.
5. They pay in a test environment.
6. They find their booking in their personal space.

Features covered:

- **Search** by category (wedding, events, corporate, real estate, drone…), by city, postcode or geolocation, by budget and by type of professional.
- **Advanced filters:** availability, rating and number of reviews, equipment, extra services, travel area.
- **Professional profiles:** portfolio, biography, services and prices, client reviews.
- **Online booking** with an availability calendar and confirmation by email and SMS.
- **Payment on the platform**, with an optional deposit set by the professional.
- **Personal spaces** for the client and for the professional.

### Planned later

- Session validation code, which releases the professional's payment.
- Messaging between client and professional.
- Graine de Champion: points, levels, rankings and badges for professionals.
- Uvision Award: photo and video competition.
- Uvision Ads: advertising slots for brands.
- Company and School accounts, calls for tenders.
- Extension to other visual professions (graphic designers, video editors, motion designers…).

### Business model

Working assumption, to be confirmed with the founders: a freemium offer for professionals and a commission on bookings.

## Tech stack

| Layer | Choice |
|---|---|
| Frontend | [Next.js](https://nextjs.org) + TypeScript + [Tailwind CSS](https://tailwindcss.com) |
| Database | [PostgreSQL](https://www.postgresql.org) |
| Authentication | [Better Auth](https://www.better-auth.com) |
| Deployment | [Vercel](https://vercel.com) |
| Payment | To be decided (Stripe Connect under study) |

## Project status

The project is just starting: this repository contains no code yet. Installation and run instructions will be added with the first version of the app.

## Repository documentation

- [`PRODUCT.md`](PRODUCT.md): product context (users, scope, constraints, open decisions).
- [`CLAUDE.md`](CLAUDE.md): working rules for designing and verifying the interface.

## Team

Project carried out by a team of ESILV students for the cofounders of Uvision.
