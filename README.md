# Fake Plastic Brands — teaser site

A lead-capture teaser for **Fake Plastic Brands**. **One job:** capture an email under a single CTA,
*get notified on release.* The product is deliberately **not out yet** — the framing is "something new is
coming," confident and withheld, never salesy.

This repo is the starting point for iterating in **Claude Design** — link it as the code source for a new
design system, then rework directly.

## The pages
| File | Concept | |
|---|---|---|
| `working-index.html` | **C · Working Index** — the teaser as a working file: a blueprint grid, a half-redacted index, a node motif. Looks like *thinking in progress.* | **recommended** |
| `transmission.html` | **A · Transmission** — the loud read: full-bleed electric blue, a giant treated headline, a broadcast "radio" lower-third. Blue as the content. | |
| `the-fold.html` | **B · The Fold** — the opposite: bone gallery-white, enormous space, one line, one hairline field, blue used exactly once. Restraint as the flex. | |
| `foundations.html` | Tokens, the three blue treatments, type stack, and the design principles. | |
| `index.html` | Contact-sheet gallery linking all three. | |

Three takes on the same teaser, differentiated across palette / type / layout / motion so a real preference
can be isolated — not one draft iterated.

## Design principles (non-negotiable)
- High-end and genuinely creative — generic/templated is the failure mode.
- Close to the creator, never a cash-grab. Over-deliver, never over-promise.
- One CTA only: capture email. Any AI stance stays **implicit** — no "use AI?" toggles.
- Single brand umbrella; the partners/consultancy path stays a discreet footer line, page is audience-first.
- Copy: dry, minimal, a little ironic. No arrows, nothing that reads AI-written.

## Tokens (locked)
- **Blue is the through-line**, treated three ways (the fork to pick): saturated field (A `#1A24E8`) / single
  restrained accent (B `#1C2A72`) / blueprint ink (C `#16225E`). Bone `#F2F0E9`, near-black ink `#13151F`.
  Sharp corners (radius 0).
- **Type:** treated/condensed grotesque (display) + mono (system text). Stand-in faces via Google Fonts
  (Anton / Archivo / JetBrains Mono). **No** Inter/Roboto/system-default, **no** Space Grotesk.
- `--font-display` is the **swap point** for the brand's real display font — drop it in and the type locks.

## ⚠️ Pending (not fabricated around)
- **The brand's real fonts + exact blue hex** aren't finalized. Faces/blues are flagged stand-ins, built as
  swappable tokens so the real assets drop in without a rebuild.
- **The email forms demo the flow but don't capture yet** — each shows a success state on submit; nothing is
  stored until the data layer is wired. The form is provider-agnostic: each `<form>` carries
  `data-endpoint="REPLACE_WITH_CAPTURE_ENDPOINT"` and a `// INTEGRATION POINT` marker.

## Live preview
- All three: https://fpb-teaser.pages.dev/
- C https://fpb-teaser.pages.dev/c/ · A https://fpb-teaser.pages.dev/a/ · B https://fpb-teaser.pages.dev/b/

## Using this in Claude Design
1. claude.ai/design → new design system → **Link code** → this repo.
2. `foundations.html` holds the tokens; the three concept pages are the components to rework.
3. Direction prompt to lock it onto the brief:

> Design a high-end teaser / lead-capture page for FAKE PLASTIC BRANDS, a creator brand with a large,
> design-literate following. One job: capture an email under a single CTA, "get notified on release." The
> product is deliberately NOT out yet — frame it as "something new is coming," confident and withheld, never
> salesy. Genuinely creative and high-end (generic is the failure mode), close to the creator, AI stance
> implicit. THROUGH-LINE: a distinctive blue, treated boldly. TYPE: a treated/condensed grotesque + a mono —
> never Inter/Roboto/system fonts, never Space Grotesk, never a rounded-card Tailwind look. TOKENS: bone
> #F2F0E9, ink #13151F, sharp corners, one CTA only, a discreet footer "partners" line, dry minimal copy with
> no arrows. Keep the three directions (Transmission / The Fold / Working Index) genuinely distinct across
> palette, type, layout and motion. Mobile + desktop. The email form posts to a provider-agnostic endpoint.
