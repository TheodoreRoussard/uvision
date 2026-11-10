# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Décidée par l'équipe :

- **Frontend :** Next.js + TypeScript + Tailwind CSS.
- **Base de données :** PostgreSQL (modèle de données et mise en place par Parikshit).
- **Authentification :** Better Auth.
- **Déploiement :** Vercel.

Encore ouvert : le prestataire de paiement (Stripe Connect à l'étude).

## Users

**Utilisateur principal (MVP) : le client particulier** qui veut réserver un photographe ou un vidéaste pour un besoin précis (mariage, événement, portrait, etc.), près de chez lui et dans son budget. Il arrive avec un besoin, une localisation et une fourchette de prix, et veut passer de la recherche à la réservation sans attendre un devis.

**Utilisateur secondaire (MVP) : le professionnel** (photographe, vidéaste, ou les deux), y compris étudiant, qui veut trouver des clients, présenter son portfolio et gérer ses disponibilités et réservations.

**Audiences futures, hors MVP :** entreprises (marques, agences, PME, startups) qui publient des appels d'offres, et écoles ou académies de formation à l'image qui gèrent leurs étudiants.

## Product Purpose

Uvision est une plateforme de mise en relation et de réservation de professionnels des métiers de l'image. Le client choisit un créatif, voit ses disponibilités et réserve un créneau.

Elle existe parce qu'accéder à un créatif est aujourd'hui lent et incertain : devis, échanges, attente.

Succès du MVP : un parcours complet et testable de bout en bout.

1. Le client recherche un photographe ou un vidéaste.
2. Il consulte son profil et son portfolio.
3. Il sélectionne une prestation et un créneau disponible.
4. Il effectue une réservation.
5. Il réalise un paiement en environnement de test.
6. Il retrouve sa réservation dans son espace personnel.

## Positioning

Réservation instantanée d'un créatif visuel, sans devis, sur une plateforme spécialisée dans les métiers de l'image. L'ambition déclarée est de créer un standard de réservation pour ce marché fragmenté, comme Planity et Doctolib l'ont fait dans leurs secteurs.

Ce que les voisins ne font pas : les réseaux sociaux donnent de la visibilité sans convertir en réservation ; les plateformes freelance généralistes sont jugées complexes et saturées.

## Operating Context

- Usage sur mobile et sur ordinateur.
- Marché de départ : la France. L'international est une ambition à terme.
- Le client cherche par ville, code postal ou géolocalisation, avec une carte interactive des résultats.
- Le jour de la prestation, client et professionnel sont ensemble sur place : c'est là que la séance est validée par un code (voir ci-dessous).
- Projet mené par une équipe étudiante pour deux cofondateurs ; le résultat doit pouvoir être repris après leur intervention (code, maquettes, documentation).

## Capabilities and Constraints

### Dans le MVP

- **Recherche** par catégorie, localisation, budget et type de professionnel ; possibilité de chercher un professionnel par son nom.
- **Catégories :** Événementiel, Sport, Corporate / Entreprise, Mode & Portrait, Immobilier, Produits / E-commerce, Lifestyle / Réseaux sociaux, Photobooth, Création vidéo / films, Drone, Voyage / nature, Technique / spécialisé.
- **Tranches de budget :** moins de 100 €, 100–200 €, 200–500 €, 500 € et plus, montant personnalisé.
- **Types de professionnel :** Photographe, Vidéaste, Photographe + Vidéaste.
- **Filtres avancés**, visibles après la première recherche : disponibilité (immédiate ou à une date), note et nombre d'avis, équipement (drone, caméra 4K…), services supplémentaires (albums imprimés…), zone de déplacement.
- **Carte de profil** dans les résultats : photo de couverture, nom et note, type de service, prix de base ou forfait, disponibilité, aperçu du portfolio.
- **Profil complet :** portfolio, biographie, description, tarifs détaillés, avis clients.
- **Réservation :** choix de la prestation et de la date, paiement en ligne, confirmation par email et SMS, suivi dans l'espace personnel du client et du professionnel.
- **Acompte**, au choix du professionnel : activable ou non, montant fixe ou pourcentage, limité à certaines prestations, avec conditions de remboursement. Le client voit clairement le montant dû immédiatement, le solde et les échéances.
- **Inscription et connexion**, profils client et professionnel, calendrier du professionnel.

### Prévu après le MVP

- **Code de validation :** le client reçoit un code unique à la réservation et le donne au professionnel en fin de séance ; la saisie du code valide la séance et débloque le paiement.
- **Messagerie** entre client et professionnel.
- **Graine de Champion (GDC) :** points par shooting, 50 niveaux, cinq groupes (Apprentis, Confirmés, Experts, Élite, Champions), classements national et international, badges, récompenses annuelles.
- **Uvision Award :** concours photo et vidéo deux fois par an, réservé aux professionnels, avec vote des inscrits.
- **Uvision Ads :** emplacements publicitaires en carrousel pour des marques, sur l'accueil, la recherche et le tableau de bord professionnel.
- **Comptes Entreprise et École**, appels d'offres et casting.
- Favoris, FAQ, blog, page partenaires, « le saviez-vous », récapitulatif annuel, comparaison de professionnels, lien vers un portfolio Behance, codes promo, désactivation temporaire de compte.
- Extension à d'autres métiers de l'image : graphistes, monteurs, motion designers, illustrateurs, retoucheurs, créateurs de contenu.
- Recommandations par intelligence artificielle.

### Contraintes

- **Vérification du professionnel :** identité, téléphone vérifié par SMS, pièce d'identité, statut (SIRET, facultatif pour les étudiants), IBAN, double authentification.
- **RGPD** et protection des données, en particulier les pièces d'identité et les données de paiement.
- **Paiement** via une solution de type marketplace ; Stripe Connect est à l'étude, rien n'est arrêté.

### Hypothèses de travail

Retenues par l'équipe pour avancer, à faire confirmer par les fondateurs car les documents sources se contredisent sur ces points.

- **Circuit de paiement :** le client paie sur la plateforme, pas directement au professionnel.
- **Modèle de revenus :** freemium pour les professionnels, plus une commission sur les réservations. Le contenu de l'offre gratuite et de l'offre payante, ainsi que le taux de commission, ne sont pas définis. Les frais annuels du cahier des charges (24 €/an étudiants, 48 €/an pros) ne sont pas repris tels quels.

### Décisions ouvertes

Les documents sources se contredisent ou restent incomplets sur ces points. Ne rien inventer : demander avant de concevoir un écran qui en dépend.

- **Devis :** la promesse est « sans devis », mais une case « PROJET » du calendrier prévoit des tarifs sur devis (clips, shootings à l'étranger).
- **Nom :** « Uvision » partout, « YouVision » mentionné une fois.
- **GDC :** rôle de la rapidité dans le score, avantages des récompenses (« à définir »), et règle des niveaux (annoncés comme ne revenant jamais à zéro alors que le score de carrière peut baisser).

## Brand Commitments

- **Nom :** Uvision.
- **Slogan :** « Réservez * Créez * Brillez ».
- **Formule de positionnement :** « Simple. Rapide. Instantané. »
- **Couleurs :** bleu, violet, gris et blanc sont une orientation initiale des fondateurs, explicitement non contraignante.
- **Liberté créative :** il n'existe ni logo, ni mascotte, ni charte graphique, ni maquette. Les fondateurs laissent volontairement l'équipe proposer sa vision ; logo, mascotte et charte font partie des pistes à explorer.

## Evidence on Hand

- `ESILV PROJET UVISION.pdf` : cahier des charges fonctionnel (19 pages).
- `ESILV SUMMARY UVISION.pdf` : résumé exécutif (équipe, projet, avantages, clientèle).
- `Re- Project Kick-off.pdf` : mail de lancement des fondateurs (vision, priorités, livrables).

Absences à ne pas combler par de l'invention : aucun logo, aucune photo ou vidéo de portfolio, aucun professionnel réel inscrit, aucun avis ou témoignage, aucun chiffre d'usage, aucun partenariat confirmé avec une marque ou une école (Canon, Sony, etc. sont cités comme cibles publicitaires, pas comme partenaires).

## Product Principles

1. **De la recherche à la réservation sans attente.** Chaque étape qui ressemble à une demande de devis ou à un aller-retour est un échec du produit.
2. **Le travail du professionnel est la preuve.** Le portfolio, les avis et le prix portent la décision du client.
3. **L'argent est toujours lisible.** Prix, acompte, solde et conditions de remboursement sont visibles avant de s'engager.
4. **La confiance se protège des deux côtés.** Professionnels vérifiés pour le client, paiement garanti pour le professionnel.
5. **Un parcours complet avant des fonctionnalités en plus.** Le MVP prime sur la gamification, la publicité et les concours.
