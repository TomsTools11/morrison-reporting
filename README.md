# Morrison Reporting

Static performance-review reports for **The Michael Morrison Insurance Agency**, on the GOAL brand system.

## Structure

- `index.html` — account hub / landing page with a card for each current report
- `reports/` — full, print-ready reports (Structured Dashboard theme):
  - `blended-performance-review.html` — Auto + Home combined, campaign launch through July 30, 2026
  - `auto-performance-review.html` — Auto campaign, campaign launch through July 30, 2026
  - `home-performance-review.html` — Home campaign, campaign launch through July 30, 2026
  - `geographic-performance-review.html` — county and city performance with a statewide county map, campaign launch through July 30, 2026
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
