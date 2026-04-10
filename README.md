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

Currently deployed to Netlify at https://bright-beijinho-c324d9.netlify.app

To deploy manually:

```bash
npx netlify-cli deploy --dir=. --prod --site=5c997035-66b7-4291-ad33-10b57b191c8b
```

(Requires `NETLIFY_AUTH_TOKEN` environment variable.)

## Notes

- No build step — pure HTML/CSS/JS
- Tenant logos in the marquee come from [logo.dev](https://logo.dev) (free tier with demo token)
- Portfolio property photos are sourced from the original Wix site CDN
