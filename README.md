# TideHouse Collective

Marketing site for TideHouse Collective, a web design & development studio in Sarasota, FL.

Static site — no build step, no dependencies. `index.html` plus a handful of assets.

## Structure

```
index.html            the whole site
favicon.svg            browser-tab icon
og-image.png           social share image (1200x630)
assets/images/logo.png wordmark used in header + footer
assets/video/hero.mp4  hero background video
robots.txt / sitemap.xml   search-engine files
.github/workflows/deploy.yml   auto-deploy to GitHub Pages on push to main
```

## Deploy

### Option A — GitHub Pages (already wired up)
1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages → Build and deployment → Source**, and select **GitHub Actions**.
3. Push to `main` (or re-run the workflow) — `.github/workflows/deploy.yml` builds and publishes automatically.
4. Your site will be live at `https://<username>.github.io/<repo>/`, or your custom domain once configured under **Settings → Pages → Custom domain**.

### Option B — Netlify / Vercel
Drag-and-drop the repo folder into Netlify, or run `vercel` / connect the GitHub repo — both auto-detect this as a static site, no config needed.

## Domain

Live at `https://tidehousecollective.com/` (custom domain on Netlify, DNS at GoDaddy, HTTPS via Netlify's auto-provisioned Let's Encrypt cert — renews automatically). `www.tidehousecollective.com` redirects to the apex.

The Netlify default URL, `https://tidehousecollective.netlify.app/`, still works and serves the same site — useful as a fallback if DNS or the custom domain ever has issues.

`index.html`'s SEO tags (`<link rel="canonical">`, `og:url`, `og:image`, `twitter:image`, JSON-LD `url`), `robots.txt`, and `sitemap.xml` all reference `tidehousecollective.com`.
