# Morrison Reporting

Static performance-review reports for **The Michael Morrison Insurance Agency**, on the GOAL brand system.

## Structure

- `index.html`: account hub / landing page with a card for each current report
- `reports/`: full, print-ready reports (Structured Dashboard theme), updated for the September 9, 2026 review:
  - `blended-performance-review.html`: Auto + Home combined, campaign launch through September 9, 2026 (year to date)
  - `auto-performance-review.html`: Auto campaign, last 30 days (August 11 to September 9, 2026)
  - `home-performance-review.html`: Home campaign, last 30 days (August 11 to September 9, 2026)
  - `source-performance-review.html`: Auto and Home lead sources, last 30 days (August 11 to September 9, 2026)
  - `blended-source-county-review.html`: Auto + Home combined by source type and by county, year to date (new 9/9/26)
  - `contact-rate-by-source-review.html`: contact rate by source type, year to date (new 9/9/26)
  - `geographic-performance-review.html`: county, metro and ZIP performance, July 15 to August 14, 2026 (retained from the 8/14 review)
- `assets/`: GOAL logo marks and `report.css`, the shared report stylesheet (every report in `reports/` links to it; it must ship with them)
- `vercel.json`: static hosting configuration

Each report has an **All Reports** back link in the top-left of its sidebar that returns to `index.html`.

Reports are generated from the GOAL Analytics CSV exports in the account folder
(`account-reviews/account-review-9-9-26/{auto,home,blended}/`). Contact, quote and bind rates are
calculated on opportunities (web leads plus inbound calls) using the call-inclusive dimension exports.

## Deployment

This is a zero-build static site deployed on [Vercel](https://vercel.com). No framework or build
step is required: Vercel serves the files directly from the repository root per `vercel.json`.

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
