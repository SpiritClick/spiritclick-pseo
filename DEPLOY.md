# Cloudflare Pages Deploy Bundle -- SpiritClick

## Contents

- **Total files in this bundle: 257** (including this DEPLOY.md)
- 246 PSEO pages (HTML) at the bundle root, preserving their original structure:
  - `/tarot/`, `/compatibility/`, `/signs/`, `/questions/` sections plus the root `index.html` hub pages
  - `sitemap.xml` and `robots.txt` at the root
- Major Arcana quiz under `/quiz/`:
  - `/quiz/index.html` plus `/quiz/assets/` (6 card images) and `/quiz/icon.webp`

## Deploy path

1. Push this bundle to a GitHub repo (the bundle root is the site root -- push the contents, not the folder).
2. In Cloudflare Pages, connect that repo. Cloudflare builds and deploys on every push; no build command or framework preset is needed (plain static files, output directory = repo root).
3. Attach the subdomain in Cloudflare Pages (Custom domains). That is the owner's one DNS step -- DNS stays with the owner; nothing else in this bundle touches DNS or the main site.

## Quiz note

The quiz must stay a single self-contained page: one `/quiz/index.html` with its `/quiz/assets/` folder beside it, exactly as bundled. Do not split it into multiple pages, extract its inline script/style into shared files, or route it through a framework -- it is designed to run as-is from the static bundle.
