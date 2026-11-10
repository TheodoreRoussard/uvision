# Uvision

**Réservez · Créez · Brillez**

Uvision est une plateforme web de mise en relation et de réservation de professionnels des métiers de l'image. Un client y trouve un photographe ou un vidéaste selon son besoin, sa localisation et son budget, consulte son portfolio, voit ses disponibilités et réserve un créneau, sans passer par un devis.

## Ce que fait l'application

### Première version (MVP)

L'objectif est un parcours complet, testable de bout en bout :

1. Le client recherche un photographe ou un vidéaste.
2. Il consulte son profil et son portfolio.
3. Il sélectionne une prestation et un créneau disponible.
4. Il effectue une réservation.
5. Il réalise un paiement en environnement de test.
6. Il retrouve sa réservation dans son espace personnel.

Fonctionnalités couvertes :

- **Recherche** par catégorie (mariage, événementiel, corporate, immobilier, drone…), par ville, code postal ou géolocalisation, par budget et par type de professionnel.
- **Filtres avancés :** disponibilité, note et nombre d'avis, équipement, services supplémentaires, zone de déplacement.
- **Profils professionnels :** portfolio, biographie, prestations et tarifs, avis clients.
- **Réservation en ligne** avec calendrier de disponibilités et confirmation par email et SMS.
- **Paiement sur la plateforme**, avec acompte optionnel défini par le professionnel.
- **Espaces personnels** pour le client et pour le professionnel.

### Évolutions prévues

- Code de validation de séance, qui débloque le paiement du professionnel.
- Messagerie entre client et professionnel.
- Graine de Champion : points, niveaux, classements et badges pour les professionnels.
- Uvision Award : concours photo et vidéo.
- Uvision Ads : emplacements publicitaires pour les marques.
- Comptes Entreprise et École, appels d'offres.
- Extension à d'autres métiers de l'image (graphistes, monteurs, motion designers…).

### Modèle économique

Hypothèse de travail, à confirmer avec les fondateurs : offre freemium pour les professionnels et commission sur les réservations.

## Stack technique

| Couche | Choix |
|---|---|
| Frontend | [Next.js](https://nextjs.org) + TypeScript + [Tailwind CSS](https://tailwindcss.com) |
| Base de données | [PostgreSQL](https://www.postgresql.org) |
| Authentification | [Better Auth](https://www.better-auth.com) |
| Déploiement | [Vercel](https://vercel.com) |
| Paiement | À décider (Stripe Connect à l'étude) |

## État du projet

Le projet démarre : ce dépôt ne contient pas encore de code. Les instructions d'installation et de lancement seront ajoutées avec la première version de l'application.

## Documentation du dépôt

- [`PRODUCT.md`](PRODUCT.md) : contexte produit (utilisateurs, périmètre, contraintes, décisions ouvertes).
- [`CLAUDE.md`](CLAUDE.md) : règles de travail pour le design et la vérification de l'interface.

## Équipe

Projet mené par une équipe d'étudiants de l'ESILV pour les cofondateurs d'Uvision.
