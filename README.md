# Morrison Reporting

Static performance-review reports for **The Michael Morrison Insurance Agency**, on the GOAL brand system.

## Structure

- `index.html` — account hub / landing page with a card for each current report
- `reports/` — full, print-ready reports (Structured Dashboard theme):
  - `auto-performance-review.html` — Auto campaign, last 30 days
  - `home-performance-review.html` — Home campaign, last 30 days
  - `geographic-targeting-overlap.html` — Texas target ZIPs vs. carrier catastrophe-exclusion list, May 2026
- `assets/` — GOAL logo marks
- `vercel.json` — static hosting configuration

Each report has an **Account hub** back link in the top-left of its sidebar that
returns to `index.html`.

## Deployment

This is a zero-build static site deployed on [Vercel](https://vercel.com). No framework or build
step is required — Vercel serves the files directly from the repository root per `vercel.json`.

Pushes to the connected branch deploy automatically. To deploy from the CLI:

```bash
vercel --prod
```

## Local preview

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
