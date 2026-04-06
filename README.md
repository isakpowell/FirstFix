# FirstFix Interiors

Static marketing website for **FirstFix Interiors** — a decorative plastering and heritage restoration business based in Hurlstone Park, Sydney, Australia.

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, services overview, featured projects, location map |
| About | `about.html` | Company story, team, values |
| Projects | `projects.html` | Portfolio gallery with project photos |
| Get a Quote | `quote.html` | Contact form and business details |

Each project also has its own detail page under `projects/`.

## Tech Stack

- **HTML/CSS/JS** — Single-file pages, all styles inline
- **Tailwind CSS** — Via CDN with custom brand config
- **Google Fonts** — Plus Jakarta Sans (headings) + Manrope (body)
- **Material Symbols** — Icon font via Google CDN
- **No build step** — Drop on any static host

## Local Development

```bash
# Start dev server (serves project root at http://localhost:3000)
node serve.mjs

# Take a screenshot (saved to ./temporary screenshots/)
node screenshot.mjs http://localhost:3000
node screenshot.mjs http://localhost:3000/about.html about
```

Requires Node.js. Puppeteer is used for screenshots only — not required to run the site.

## Deployment

The site is deployed on **Netlify**. The `_headers` file sets security headers and cache-control rules automatically.

### Files included for deployment

```
_headers      # Netlify HTTP headers (security + caching)
robots.txt    # Search engine crawl rules
sitemap.xml   # All pages with priorities and lastmod dates
```

## Project Structure

```
FirstFix/
├── index.html
├── about.html
├── projects.html
├── quote.html
├── sitemap.xml
├── robots.txt
├── _headers
├── serve.mjs
├── screenshot.mjs
├── brand_assets/
│   ├── logo.png
│   └── favicon.png
└── projects/
    ├── paddington-project/
    ├── stanmore-project/
    └── ...
```

## SEO

- Meta title/description on every page
- Open Graph + Twitter Card tags
- JSON-LD structured data: `LocalBusiness`, `WebSite`, `Service`, `BreadcrumbList`
- Canonical URLs
- Sitemap + robots.txt
- Hero image preloaded with `fetchpriority="high"`
- All below-fold images use `loading="lazy"`

## Brand

Business details:
- **ABN:** 56 680 254 083
- **Phone:** 0450 083 182
- **Location:** Hurlstone Park, Sydney NSW
- **Service area:** Sydney's Inner West and surrounds
