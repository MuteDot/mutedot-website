# MuteDot website

Static site: plain HTML and CSS, no JavaScript, no build step. The hero demo is pure CSS.

```
index.html          landing page
privacy/ terms/ refunds/   legal pages
buy/index.html      redirect to checkout (the only place the checkout link lives)
404.html            not-found page
css/site.css        all styles
logo/svg/           lockups from the brand kit (unchanged)
favicon.*, apple-touch-icon.png, icon-*.png, og-image.png, site.webmanifest
```

## Before you launch

Find and replace these placeholders across the folder:

| Placeholder      | Where                                   |
|------------------|-----------------------------------------|
| `[CHECKOUT_URL]` | `buy/index.html` only (Lemon Squeezy or Polar link) |
| `[DOMAIN]`       | canonical and Open Graph tags           |

Every Buy button links to `buy/`, which redirects to `[CHECKOUT_URL]`, so the checkout link is set in one file and works without JavaScript.

`og-image.png` (and the Product Hunt images in the kit) still say "macOS · Windows · Linux". Re-export them without macOS before launch.

The legal pages are plain-language starting points, not legal advice.

## Deploy

Publish the repo root as the site. No build command is needed.

- **Netlify / Cloudflare Pages:** publish directory `/` (repo root), no build command
- **Vercel:** framework preset "Other", output directory `.`
- **GitHub Pages:** serve from the `main` branch root with a custom domain. The favicon and 404 paths are root-relative (`/favicon.ico`), so a `username.github.io/repo/` project URL would break them.
