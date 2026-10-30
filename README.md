<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="logo/svg/mutedot-lockup-color-on-dark.svg">
  <img src="logo/svg/mutedot-lockup-color.svg" alt="MuteDot" width="360">
</picture>

### The marketing site for MuteDot.<br>Plain HTML and CSS. No JavaScript, no build step.

<br>

![HTML + CSS](https://img.shields.io/badge/HTML%20%2B%20CSS-static-110F14?style=flat-square&labelColor=FF5F15)
![No JavaScript](https://img.shields.io/badge/JavaScript-none-110F14?style=flat-square&labelColor=FF5F15)
![No build step](https://img.shields.io/badge/build-none-110F14?style=flat-square&labelColor=5E5966)
![No cookies](https://img.shields.io/badge/cookies-none-110F14?style=flat-square&labelColor=5E5966)
![Fonts](https://img.shields.io/badge/fonts-Sora%20%C2%B7%20Inter%20%C2%B7%20JetBrains%20Mono-110F14?style=flat-square&labelColor=5E5966)

<br>

<img src=".github/readme/hero.png" alt="The MuteDot homepage: a floating glass nav, the headline 'Never get caught on a hot mic.' and a glass window demoing the LIVE indicator and the Ctrl Shift M hotkey" width="800">

</div>

<br>

## ✦ Pages

| Path | What it is |
|---|---|
| `index.html` | Landing page. The hero demo is pure CSS. |
| `privacy/` · `terms/` · `refunds/` | Legal pages |
| `buy/index.html` | Redirects to checkout. It's the only place the checkout link lives. |
| `404.html` | Not-found page |
| `css/site.css` | Every style on the site |
| `logo/svg/` | Lockups from the brand kit, unchanged |
| `favicon.*` · `apple-touch-icon.png` · `icon-*.png` · `og-image.png` · `site.webmanifest` | Icons and social card |

<br>

## ✦ Design

The site uses the brand kit's bold blocks of **Ink**, **Paper** and **Hot Orange**, plus macOS-style liquid glass:
a floating capsule nav, and frosted windows with lit rims sitting over solid orange dots taken from the logo.

<img src=".github/readme/settings.png" alt="The features section: a glass copy of MuteDot's Settings window with Shortcuts, Indicator and General options, beside a glass terminal running mutedot --status and --toggle" width="800">

The Settings window and the terminal on the page copy the real app. They use the same rows,
hints and defaults as the app's Settings window, and the same CLI flags.
**If the app's settings change, update this section too.**

<details>
<summary><b>Brand tokens</b></summary>
<br>

| Token | Hex | Use |
|---|---|---|
| Hot Orange | `#FF5F15` | CTAs, highlights, the dot. Text on orange is always Ink. |
| Ink | `#110F14` | Text, dark sections |
| Paper | `#F7F4EF` | Light background |
| Night | `#1C1A21` | Surfaces on dark |
| Ember | `#B93A06` | Orange for small text and links on light |
| Slate | `#5E5966` | Secondary text on light |
| Mist | `#A8A3B0` | Secondary text on dark |
| Live / Muted | `#22C55E` / `#EF4444` | **The indicator only** |

Type: **Sora** for headings, **Inter** for body text, **JetBrains Mono** for keys and code.

</details>

<br>

## ✦ Before you launch

The domain is **mutedot.xyz**, set in `CNAME` and used in the canonical and Open Graph tags.
One placeholder is left:

| Placeholder | Where |
|---|---|
| `[CHECKOUT_URL]` | `buy/index.html` only (Lemon Squeezy or Polar link) |

Every Buy button links to `buy/`, which redirects to `[CHECKOUT_URL]`. That way the checkout link is set in one file and works without JavaScript.

> [!WARNING]
> `og-image.png`, along with the Product Hunt images in the brand kit, still says "macOS · Windows · Linux".
> Re-export them without macOS before launch.

> [!NOTE]
> The legal pages are plain-language starting points, not legal advice.

<br>

## ✦ Deploy

Publish the repo root as the site. No build command is needed.

| Host | Settings |
|---|---|
| **Netlify / Cloudflare Pages** | Publish directory `/` (repo root), no build command |
| **Vercel** | Framework preset "Other", output directory `.` |
| **GitHub Pages** | Serve from the `main` branch root. `CNAME` already sets the custom domain. |

The favicon and 404 paths are root-relative (`/favicon.ico`), so a `username.github.io/repo/` project URL would break them. Use a custom domain.

<br>

<div align="center">
<sub>© 2026 Aubergine-UX. All rights reserved.</sub>
</div>
