# Morrison Reporting

Static performance-review reports for **The Michael Morrison Insurance Agency**, on the GOAL brand system.

## Structure

- `index.html` — landing page comparing the three report themes
- `reports/` — three full, print-ready report treatments (Refined Light, Navy Editorial, Structured Dashboard)
- `assets/` — GOAL logo marks
- `vercel.json` — static hosting configuration

> The reports currently contain placeholder data.

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
