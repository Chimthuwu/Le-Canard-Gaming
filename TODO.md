# Le Canard Gaming — Amy Birdhouse's Duck Pond Website

## Summary
Single-page, self-contained cinematic website for streamer Amy Birdhouse
("Le Canard Gaming" — DOTA 2 / Age of Empires II / ducks). Original brief:
`C:\Users\Serge\Desktop\Claude — Le Canard Gaming Master Website Prompt.md`.
Entry point is `index.html` (root) + `assets/`.

- Live: https://le-canard-gaming.pages.dev
- Repo: https://github.com/Chimthuwu/Le-Canard-Gaming
- Cloudflare: classic Pages project `le-canard-gaming` (account
  Chimske@gmail.com's Account). Deploy with:
  `npx wrangler pages deploy . --project-name=le-canard-gaming`
  (deploys only tracked-looking site files; classic Pages auto-excludes
  `.git`/`node_modules`, unlike the newer Workers-assets path — do NOT use
  `wrangler deploy` or `wrangler pages project create` without `--force`
  here, it redirects to Workers-assets and will upload `.git` publicly).

## Status: live, iterating on feedback

## Done
- Full site per the master brief: intro cinematic + replay, pond
  environment (moon/reeds/fireflies/water/tint-per-section), hero, live
  section, community/schedule, Amy section, Inner Circle request portal
  ("THE DEEP WATER"), socials, footer, hidden-duck discovery game with a
  mascot duck (arrow-key easter egg), a11y + reduced-motion + mobile.
- DOTA 2 / Age of Empires II "world" sections were built per the brief,
  then **removed** at the user's request (2026-09-12) — cut entirely, not
  just hidden. Related CSS (`.game-world`, `.world-*`, embers/torches) and
  the nav "Games" link were removed too.
- Hero centerpiece swapped from a hand-drawn SVG blob (user: "this doesn't
  look like a duck at all") to `assets/DuckIcon.png` floating on animated
  water rings.
- Social preview metadata added (OG/Twitter) with a generated 1200x630
  thumbnail at `assets/og-image.png` (built from a temp HTML card,
  screenshotted headlessly via local Edge — see git history if it needs
  regenerating).
- GitHub repo created (public) and pushed; deployed to Cloudflare Pages.

## Next / open questions
- User said Discord user ID `821485604864524288` is Amy's — not yet wired
  into anything (unclear if it should become the "Join Discord" link,
  which currently is still a `#` placeholder in `CONFIG.discordUrl`, or is
  meant for something else like a future backend notification target for
  the request portal). Ask before using it as a public-facing link.
- Real socials/Twitch/Discord invite URLs and `CONFIG.requestEndpoint`
  (backend for the Inner Circle request form) still placeholders.
- Real portrait photo for the Amy section (currently a designed
  placeholder frame, per the brief — no fabricated photo).
- Custom domain not set up; currently only `*.pages.dev`.

## Known quirk (not a site bug)
While QA-ing in this session, the Claude-in-Chrome extension's own
screenshot capture occasionally rendered stale/tiled frames or phantom
gray overlay boxes over certain absolutely-positioned elements. Confirmed
via `getComputedStyle` (backgrounds were transparent) and via a clean
headless Edge screenshot of the same page — it's an artifact of that
automation tooling, not the page.
