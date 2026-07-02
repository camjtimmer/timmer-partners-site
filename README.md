# Timmer Partners Website

Marketing site for Timmer Partners — industrial real estate capital (acquisitions, sale-leasebacks, partnerships, and debt).

## Structure

- `index.html` — Homepage (hero, track record, tenants, capital solutions, portfolio preview, testimonials, contact CTA)
- `portfolio.html` — Full portfolio with state filters and tenant deep links (`?tenant=slug`)
- `404.html` — Branded not-found page
- `styles.css` — All styles (design tokens at the top; bump the `?v=` query in the HTML when shipping structural CSS changes)
- `brand/` — Logo lockups, favicon, apple-touch-icon, stationery SVGs
- `photos/` — Property photography (resized to ~800px with `sips -Z 800`)
- `hero-industrial.jpg` — Homepage hero; `og-image.jpg` — 1200×630 social share image
- `robots.txt`, `sitemap.xml` — SEO plumbing (point at timmerpartners.com)

## Local preview

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080

## Deploying

Live at https://camjtimmer.github.io/timmer-partners-site/

Auto-deploy via GitHub Pages (`.github/workflows/pages.yml`). Every push to `main` deploys in about a minute:

```bash
git add .
git commit -m "your change"
git push
```

## Notes

- No build step — pure HTML/CSS/JS
- Tenant logos come from [logo.dev](https://logo.dev) (attribution link in the footer is required by their free tier); each `<img>` has an `onerror` fallback that hides it if the CDN fails
- All property photos are hosted locally in `photos/`
- Custom domain (timmerpartners.com) not yet attached — canonical/OG URLs already point at it
