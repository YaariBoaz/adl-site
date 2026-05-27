# ADL — adl.solutions

Corporate site for ADL Training Solutions. Single-page static site with no build step or dependencies (beyond Google Fonts via CDN).

## File structure

```
adl-site/
├── index.html              Main page (self-contained: HTML + CSS + JS inline)
├── favicon.svg             SVG favicon
├── favicon-32.png          PNG fallback
├── apple-touch-icon.png    iOS home-screen icon
├── robots.txt              SEO — allow all
├── sitemap.xml             SEO — single-page sitemap
└── assets/
    ├── demo.mp4            Hero background video (Cinema Mode @ LE"B)
    ├── demo-poster.jpg     Video poster (shown before video loads)
    ├── targo-splash.png    App: splash screen
    ├── challenge-intro.png App: challenge brief
    ├── shooting-live.png   App: live shot detection
    ├── stats-overview.png  App: stats + leaderboard
    └── ...                 Other product screens (kept for future use)
```

## Local preview

Any static server works. From this directory:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to Vercel (recommended)

1. Create a new GitHub repo named `adl-site` and push the contents of this folder.
2. Go to [vercel.com](https://vercel.com) → **Add New Project** → import the repo.
3. Framework preset: **Other**. Build settings: leave blank. Output directory: leave blank.
4. Click **Deploy**. You'll get a free `adl-site-xxxxx.vercel.app` URL within 60 seconds.

## Connecting adl.solutions when ready

1. In Vercel: Project → Settings → Domains → Add `adl.solutions` and `www.adl.solutions`.
2. Vercel will show DNS records to add at the domain registrar (typically an A record + CNAME).
3. Add them at the registrar. Propagation takes 5–60 minutes. Vercel will auto-issue an SSL cert.

## What's in / what's out

**In:** $3.5M defense contract, 290-range pipeline, pilot metrics (500+ users, 40% conversion), LE"B deployment, market sizing ($15.4B defense + ~$600M U.S. SAM), team + advisor + existing backers.

**Out (deck-only):** $9M ask, $30M pre-money, EBITDA table, internal revenue projections, Cinema Suite / Pin-Point Lane pricing, 77% gross margin, use-of-funds breakdown.

## Editing copy

All text is in `index.html`. Section anchors:

| Anchor       | Section                       |
|--------------|-------------------------------|
| `#top`       | Hero                          |
| `#why`       | 01 — Why Now                  |
| `#platform`  | 02 — The Platform             |
| `#defense`   | 03 — Defense Validation       |
| `#civilian`  | 04 — Civilian Traction · Targo |
| `#roadmap`   | 05 — Product Roadmap          |
| `#markets`   | 06 — The Markets              |
| `#competition` | 07 — Competition & Moat     |
| `#team`      | 08 — Team & Backers           |
| `#contact`   | Contact                       |

## Design tokens (CSS variables)

Defined at the top of `index.html`:

| Token        | Value     | Purpose                       |
|--------------|-----------|-------------------------------|
| `--bg`       | `#0d0e12` | Night black background        |
| `--gold`     | `#e6a817` | Targo gold accent             |
| `--defense`  | `#6b8aa8` | Cool tone for defense section |
| `--text`     | `#e9eaee` | Primary text                  |
| `--text-dim` | `#8b8f9a` | Secondary text                |

## Performance notes

- Hero video: 717 KB (optimized from 4.5 MB), H.264 MP4 with faststart
- Total page weight: ~1.2 MB including all images
- No external dependencies except Google Fonts (Fraunces + Inter + JetBrains Mono)
- Reveal-on-scroll animations gracefully degrade if JS is disabled

## Contact

Site content questions → boaz@adl.solutions (or alon@adl.solutions for business)
