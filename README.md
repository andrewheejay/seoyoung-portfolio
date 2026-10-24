# Seoyoung Jin — Portfolio

Static portfolio site. No build step: `index.html`, `styles.css`, `images/`, and the resume PDF are served as-is from the repo root via GitHub Pages.

To update a photo, replace the file in `images/` under the same filename and push.

## Handoff notes

### Section 01, step 04 — "Community-funded winter relief"

Below the stats row and the lede, the photos sit in two flex rows (`.row.relief-row`: `display: flex; gap: 24px; align-items: flex-start; margin-top: 24px`). Each figure's `flex-grow` is its photo's width ÷ height and every frame's `aspect-ratio` is the photo's real proportion, so the two photos in a row share one height and nothing is cropped.

- Row A (two portraits): the safety poster `winter-guide.png` (1400×1986, `flex: .705`, bordered `<img>`) and `hot-water-bottles.webp` (245×436, `flex: .562`, `.frame`).
- Row B (two landscapes): `in-person-guidance.webp` (610×457, `flex: 1.335`, `.frame`) and `handover.jpg` (1800×1350, `flex: 1.333`, full-bleed 4:3 `<img>`, no border).

Below 520px both rows wrap and each figure becomes full width (the same `.row` rule section 03 uses).

### Assets (`images/`)

Final: `coasters-night.jpg`, `painting-cranes.jpg`, `materials.jpg`, `coasters-gold.jpg`, `coasters-sunset.jpg`, `coasters-magnolia.jpg`, `flute-echo.jpg`, `hallway.jpg`, `lunchbox.jpg`, `kakao.jpg`, `winter-guide.png` (1400×1986), `handover.jpg` (1800×1350), `volleyball.jpg`, `team.jpg`.

**Low-resolution — replace before launch.** These only exist as small WebP previews (the hero is 1200×900). Re-export the originals under the same filenames and nothing else needs to change:
`library-of-proust.webp` (hero), `hypothermia-review.webp`, `hot-water-bottles.webp` (245×436), `in-person-guidance.webp` (610×457), `gingerbread-houses.webp`, `sports-day.webp`, `thank-you-card.webp`, `shoebox-drive.webp`, `winter-kits.webp`, `lab-myongji.webp`, `catalyst-synthesis.webp`, `lab-day.webp`, `test-cell.webp`, `polarization-curve.webp`, `lab-onboarding.webp`, `reading-results.webp`, `rexto.webp`. If an original has a different aspect ratio than the preview, re-check its crop (`object-position` / the `.zoom` values).

Other: `Seoyoung-Jin-Resume.pdf` (linked twice). Fonts load from Google Fonts.
