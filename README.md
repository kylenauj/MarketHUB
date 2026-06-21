# OCS Suite — Market Hub

Internal dashboard hub for OCS wholesale pricing and sales data.

## Tools

- **`index.html`** — dashboard shell (start here)
- **`pricing-intelligence.html`** — landed-cost calculator & market price positioning
- **`wholesale-dashboard.html`** — monthly OCS sales trends, rankings, comparisons
- **`vape-flavour-intelligence.html`** — fruit-flavour share & SKU performance for vapes

## Shared Data

Click **Shared Data** in the sidebar (or top bar) and drop your monthly OCS export
files in once. They're parsed locally in your browser, saved to IndexedDB so they
survive a reload, and automatically pushed into whichever tool you switch to —
no need to upload the same files separately in each one.

- **Pricing Intelligence** — most recently dated file becomes the Market Pricing
  snapshot; the full set feeds the Trends tab.
- **Wholesale Dashboard** — files run through its normal monthly import (column
  auto-detect + per-period storage), same as dragging them into its own uploader.
- **Vape Flavour Intelligence** — files load in, then its column mapper appears
  once for you to confirm before it builds the flavour breakdown.

Remove a file or hit **Clear all** in the Shared Data panel to reset — the active
tool reloads automatically to reflect the change. Each tool's own upload zone
still works too, if you ever want to load something into just one of them.

## Running it

This is a static site — no build step. The shell loads each tool into an iframe by relative path, so all four files need to stay together in the same folder.

**Locally:** don't just double-click `index.html` — some browsers block local iframes opened via `file://`. Run a quick local server from this folder instead:

```
npx serve .
```

**Live:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) or import the repo into Vercel. Either will serve it correctly.
