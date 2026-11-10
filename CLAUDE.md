# UVISION

## Scoping documents

The PDFs at the root describe the features expected from the app (structure and scope, not design). They are confidential and excluded from the repository by `.gitignore`: they exist only on machines where they were copied.

- `ESILV PROJET UVISION.pdf`
- `ESILV SUMMARY UVISION.pdf`
- `Re- Project Kick-off.pdf`

They are the authority on the *what* (features, scope). `PRODUCT.md` is their design-oriented summary: update it if the PDFs change. On the visual side, they give only a non-binding orientation (blue, purple, grey, white); the visual direction will be set in `DESIGN.md`.

## Frontend design: one role per tool

- Every design decision (visual direction, typography, colours, layout, animation) goes through the `impeccable` skill. `PRODUCT.md` and `DESIGN.md` are the authority.
- Do not invoke `frontend-design` on this project: it would duplicate impeccable and ignore `DESIGN.md`.
- For a UI task, `impeccable shape` replaces `superpowers:brainstorming`.
- `playwright-skill` is for verification only: responsive screenshots (375 / 768 / 1440 px, light and dark themes), journey tests, links. It neither decides nor changes the design.
- To compare visual variants, use `impeccable live` or `generate`, not Playwright.

## UI workflow

1. Frame: `impeccable init` (once), then `impeccable shape <feature>`.
2. Build with impeccable alone.
3. Capture the rendered result with Playwright at the three widths.
4. Judge with `impeccable critique` or `audit` from those screenshots.
5. Fix with the matching impeccable command (`polish`, `layout`, `adapt`, etc.).
6. Validate with Playwright: full journeys and new screenshots, to confirm there is no regression.
