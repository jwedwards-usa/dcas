# DCAS

Daily DCA allocation snapshot and static viewer.

This repo keeps the latest DCA signal export in `latest-dcas.json` and publishes
a small dependency-free GitHub Pages app from `docs/`. The app reads the latest
JSON export, converts below-line DCAS values into buy-strength scores, applies
the daily budget/minimum-allocation rules, and shows the resulting daily allocations.
The allocation score uses negative `dcasValue` readings below the visible zero
line; visual red/green color is tracked separately as additional DCAS context.
Each row also includes `lastDecodedDailyCandleClosePrice` from the latest decoded
TradingView daily candle in the position-view sidecar.

Live page: https://jwedwards-usa.github.io/dcas/

## Files

- `latest-dcas.json`: current asset DCAS value, line side, and visual color data used by the page.
- `docs/index.html`: static allocation viewer.
- `.github/workflows/pages.yml`: GitHub Pages deployment workflow.
