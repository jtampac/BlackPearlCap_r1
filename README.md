# Black Pearl Capital — Website

A multi-page institutional website for **Black Pearl Capital**, a global multi-family
office and co-investment platform. Hand-built, dependency-free, GitHub Pages ready.

## Pages

- `index.html` — Home: executive summary (hero, leadership preview, firm, key figures, approach preview, global-presence preview, contact CTA)
- `about.html` — About: firm story, key figures, track record
- `leadership.html` — Leadership: founder profiles + career timelines
- `approach.html` — Investment Approach: philosophy, focus sectors, portfolio
- `presence.html` — Global Presence: interactive world map, offices, live local times
- `contact.html` — Contact: offices, live local times, network map, enquiries

## Structure

```
black-pearl-capital/
├── *.html (six pages)        consistent header/footer, active nav per page
├── .nojekyll · README.md
├── assets/
│   ├── css/styles.css        design tokens + all styling
│   ├── js/main.js            nav, hero, maps, markers, clocks, filters, reveals
│   └── img/logo-mark.svg     three-pearl brand mark (also favicon)
└── components/
    ├── world-map.js          dotted map + routes + capital-flow packets
    └── reveal.js             scroll reveals + counters
```

All pages share one stylesheet and the same JS, which initialises only the features
present on each page (maps, clocks, filters, counters degrade gracefully when absent).

## Branding

The full name **Black Pearl Capital** renders everywhere in one uniform serif wordmark;
the gold accent lives on the three-pearl mark. The name never clips, down to 320px.

## Deploy (GitHub Pages)

Push to a repo → Settings → Pages → Deploy from branch → `main` / root. The `.nojekyll`
file ensures `assets/` and `components/` are served verbatim. Locally: `python3 -m http.server`.

## Founder photography

Monogram + engraved guilloché is the default. To use real photos, uncomment the
`<img class="founder__photo" src="assets/img/<name>.jpg">` line in each founder block
(`index.html`, `leadership.html`); it fills via `object-fit: cover` and hides the monogram.

Content reflects the firm's public information; presented for demonstration, not advice.
