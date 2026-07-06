# DCAS

Daily DCA allocation snapshot and static viewer.

This repo keeps the latest DCA signal export in `latest-dcas.json` and publishes
a small dependency-free GitHub Pages app from `docs/`. The app reads the latest
JSON export, converts delta values into buy-strength scores, applies the daily
budget/minimum-allocation rules, and shows the resulting daily allocations.

Live page: https://jwedwards-usa.github.io/dcas/

## Files

- `latest-dcas.json`: current asset delta data used by the page.
- `docs/index.html`: static allocation viewer.
- `.github/workflows/pages.yml`: GitHub Pages deployment workflow.
