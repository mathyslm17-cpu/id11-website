# ID11 — site v2

Built from the Canva architecture whiteboard. Static HTML + one stylesheet. No build step,
no dependencies — every file here can be edited directly in the GitHub web UI.

## What's in here

| | |
|---|---|
| `index.html` | Homepage — the trailer. 12 sections in the whiteboard's order. |
| `assessment.html` | The six-step assessment. |
| `contact.html`, `thanks.html`, `404.html` | Utility pages. |
| 20 content pages | One per underlined whiteboard item, built from its post-it. |
| `assets/id11.css` | The whole design system. One file. |
| `assets/` | Photos, club crests, confederation logos, alumni, logo SVGs, OG image. |
| `netlify.toml`, `robots.txt`, `sitemap.xml` | Deploy config and SEO. |

## Deploying (replacing what's on Netlify now)

1. In your GitHub repo, delete everything at the root.
2. Upload the **contents** of this folder to the repo root — not the folder itself.
   `index.html` must sit at the top level, with `assets/` beside it.
3. Commit. Netlify redeploys automatically.
4. In Netlify: **Base directory** empty, **Publish directory** `.` — nothing nested.

## Navigation

Five dropdowns matching your whiteboard grouping, plus Contact and the CTA:

- **About** — About ID11, Leadership, Our Impact, Alumni, Media, Beyond the 11
- **Pathways** — The Pathway, Study & Play, Paris/Málaga/Cologne, Pro Contracts, Events
- **Network** — Clubs, Club Partnerships, Academy Partners, Universities & Colleges
- **Foundation** — The Foundation, Scholarships, Foundation Partners
- **Partner** — Why Partner With ID11, Commercial & Brands

Below 1180px this collapses into a full-screen menu with the same grouping.

## Forms

Three Netlify forms: `start` (homepage card), `assessment` (six steps), `contact`.
All redirect to `/thanks.html`. All have honeypots. **Turn on email notifications**
in Netlify → Forms → Settings, or submissions sit in the dashboard unread.

## Mobile

Every phone rule lives in one block at the bottom of `assets/id11.css`
(`@media(max-width:699px)`, then `@media(max-width:380px)`). It is last in the
cascade on purpose — anything you add above it will be overridden on phones,
which is the behaviour you want.

Checked at 390 / 768 / 1440: no horizontal overflow on any of the 25 pages.

## Still outstanding

- **Willem II crest** — not in the crest pack you sent, so it's not in the club wall.
- **Real contact email** — every page currently points at `info@id11.org`.
- **Photography** — the alumni and hub shots are the ones you sent; higher-res versions
  would help the large blocks. Rights confirmation still needed on the Marbella landscape.
- **French translation** — the language switcher is wired up visually but only EN exists.
- **Leadership names** — the page is structured for real profiles; none are invented.
- **Site visibility** — the Netlify site still returns 401. Set it to public.

## A note on the copy

Nothing on these pages claims a fact I couldn't source from your own decks or verify.
Where a page needs a number you haven't given me (scholarship counts, named staff,
partner institutions), the copy describes what will go there rather than inventing it.
Every figure is dated "as of August 2026", per your brand guide.
