# Le Canard Gaming — Amy Birdhouse's Duck Pond Website

## Summary
Single-page, self-contained cinematic website for streamer Amy Birdhouse
("Le Canard Gaming" — DOTA 2 / Age of Empires II / ducks). Brief lives in
`C:\Users\Serge\Desktop\Claude — Le Canard Gaming Master Website Prompt.md`.
Core rule: **the pond IS the site** — content emerges from an animated
nighttime pond environment, not cards on a background image.

Assets in `assets/` are a mix of:
- a pixel-art teal duck fighter spritesheet (idle/walk/jump/attacks/etc,
  64x64 frames, several 4-frame strips) — used as the "mascot" duck you can
  walk around with arrow keys (secret keyboard interaction).
- `DuckIcon.png` — used as favicon.
- misc rubber-duck / pond renders (`Ducks-ponds*.png`, `bubbles.png`) — not
  used in v1 (primary visual language is CSS/SVG per brief); kept in case we
  want raster flourishes later.
- No real photo of Amy exists — portrait section uses a designed placeholder
  frame, not a fabricated photo.

## Status: v1 build in progress

## Now
- [ ] Build `le-canard-gaming.html` (single self-contained file) with:
  intro cinematic + replay, pond-world background, hero, duck discovery,
  live section, DOTA world, AOE world, community/pond, schedule, Amy,
  Inner Circle request portal ("THE DEEP WATER"), socials, footer,
  a11y + reduced-motion + mobile recomposition.

## Next
- [ ] Open in browser, sanity-check animations, reduced-motion, mobile width,
  keyboard interaction, duck-discovery persistence.
- [ ] Wire real socials/Twitch/Discord URLs and `requestEndpoint` once Amy
  provides them (currently placeholders in the `CONFIG` object at top of
  the `<script>`).

## Later / open questions
- Real portrait photo for the Amy section.
- Real Twitch API integration for live status (frontend is structured for
  it — see `CONFIG` and the `renderLiveState()` function — but currently
  shows static demo data).
- Backend for the request portal (`CONFIG.requestEndpoint`) — currently a
  demo-only intercepted submit, no network call, no payment handling.
