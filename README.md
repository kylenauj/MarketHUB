# OCS Suite — Buddy Blooms

Internal dashboard hub for OCS wholesale pricing and sales data.

## Tools

- **`index.html`** — dashboard shell (start here)
- **`pricing-intelligence.html`** — landed-cost calculator & market price positioning
- **`wholesale-dashboard.html`** — monthly OCS sales trends, rankings, comparisons
- **`vape-flavour-intelligence.html`** — fruit-flavour share & SKU performance for vapes

## Running it

This is a static site — no build step. The shell loads each tool into an iframe by relative path, so all four files need to stay together in the same folder.

**Locally:** don't just double-click `index.html` — some browsers block local iframes opened via `file://`. Run a quick local server from this folder instead:

```
npx serve .
```

**Live:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) or import the repo into Vercel. Either will serve it correctly.
