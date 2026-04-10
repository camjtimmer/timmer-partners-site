# Timmer Partners Website

Marketing site for Timmer Partners — industrial sale-leaseback and creative capital solutions.

## Structure

- `index.html` — Homepage (hero, stats, tenant marquee, capital solutions, portfolio preview, process, testimonials, CTA)
- `portfolio.html` — Full portfolio page with all properties
- `hero-property.jpg` — Hero background image
- `logo-*.{png,jpg}` — Brand assets

## Local preview

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080

## Deploying

Live at https://bright-beijinho-c324d9.netlify.app

Auto-deploy is wired up via Netlify. Every push to `main` triggers a new production build within ~10 seconds. No manual deploy commands needed — just:

```bash
git add .
git commit -m "your change"
git push
```

## Working from another computer

```bash
git clone https://github.com/camjtimmer/timmer-partners-site.git
cd timmer-partners-site
python3 -m http.server 8080  # local preview
```

## Notes

- No build step — pure HTML/CSS/JS
- Tenant logos in the marquee come from [logo.dev](https://logo.dev) (free tier with demo token)
- Portfolio property photos are sourced from the original Wix site CDN
