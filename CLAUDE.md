# UVISION

## Documents de cadrage

Les PDF à la racine décrivent les fonctionnalités attendues de l'app (structure et périmètre, pas le design). Ils sont confidentiels et exclus du dépôt par `.gitignore` : ils n'existent que sur les machines où on les a copiés.

- `ESILV PROJET UVISION.pdf`
- `ESILV SUMMARY UVISION.pdf`
- `Re- Project Kick-off.pdf`

Ils font autorité sur le *quoi* (fonctionnalités, périmètre). `PRODUCT.md` en est le résumé orienté design : le mettre à jour si les PDF changent. Côté visuel, ils ne donnent qu'une orientation non contraignante (bleu, violet, gris, blanc) ; la direction visuelle sera fixée dans `DESIGN.md`.

## Design frontend : un rôle par outil

- Toute décision de design (direction visuelle, typographie, couleurs, layout, animation) passe par le skill `impeccable`. `PRODUCT.md` et `DESIGN.md` font autorité.
- Ne pas invoquer `frontend-design` sur ce projet : il ferait doublon avec impeccable et ignorerait `DESIGN.md`.
- Pour une tâche d'UI, `impeccable shape` remplace `superpowers:brainstorming`.
- `playwright-skill` sert uniquement à vérifier : captures responsive (375 / 768 / 1440 px, thèmes clair et sombre), tests de parcours, liens. Il ne décide ni ne modifie le design.
- Pour comparer des variantes visuelles, utiliser `impeccable live` ou `generate`, pas Playwright.

## Flux de travail UI

1. Cadrer : `impeccable init` (une fois), puis `impeccable shape <fonctionnalité>`.
2. Construire avec impeccable seul.
3. Capturer le rendu avec Playwright aux trois largeurs.
4. Juger avec `impeccable critique` ou `audit` à partir de ces captures.
5. Corriger avec la commande impeccable adaptée (`polish`, `layout`, `adapt`, etc.).
6. Valider avec Playwright : parcours complets et nouvelles captures, pour confirmer l'absence de régression.
