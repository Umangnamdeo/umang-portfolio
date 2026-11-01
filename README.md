# Umang Namdeo — Portfolio

A single-file interactive portfolio website for **Umang Namdeo**, CS student, footballer, and creative developer. Projects sync automatically from the GitHub API; no manual deployment is needed when new repos are pushed.

🔗 **Live site:** https://umang-portfolio-seven-flax.vercel.app

---

## Features

| Feature | Detail |
|---|---|
| **Live GitHub sync** | Fetches all public repositories from `github.com/Umangnamdeo` via the GitHub API on every page load. New repos appear automatically; deleted or private repos disappear. Handles pagination (100 repos/page), ETags, caching, rate-limiting, and offline fallback. |
| **Interactive canvas visuals** | Every project card has a unique, interactive 2D canvas illustration: drag or tap to interact. Euler-3D shows a steerable vortex field; AeroStudio shows drag-driven streamlines; AudioSplit shows tappable stem lanes with a playhead; Sonic-Space shows a spatial listener you can move. |
| **Scroll-driven animations** | Three major scroll sequences: cinematic hero parallax, immersive project showcase with 3D card depth, and a convergence journey leading into the contact section. |
| **About section accordions** | Expandable rows in the About section each run a live canvas visual alongside a short description. |
| **Responsive** | Tested at 360 px, 390 px, 768 px, 1366 px, and 1920 px. Mobile CTAs stack full-width below 480 px. |
| **Reduced-motion** | All animations pause when `prefers-reduced-motion: reduce` is set. The page remains fully readable and navigable. |
| **Performance** | Animations are `transform`/`opacity`-only. Canvas loops are gated by `IntersectionObserver`; off-screen canvases pause. Low-power devices (≤ 4 CPU cores or < 768 px) use reduced particle counts and a lower DPR cap. |
| **Accessibility** | Semantic landmarks, `aria-label`/`aria-expanded`/`aria-live` throughout, visible focus outlines, skip-to-content link, keyboard-navigable accordion rows. |
| **SEO** | Unique `<title>` and `<meta description>`, Open Graph tags, JSON-LD `Person` and `WebSite` structured data, configurable canonical URL via `SITE_URL`. |

---

## Projects (synced from GitHub)

Projects are fetched live. The ones below were verified at the time the site was built:

| Project | Status | Stack (confirmed) | Stack (reported) |
|---|---|---|---|
| **Euler-3D** | Live demo | TypeScript | WebGL, GLSL, React 19 |
| **AeroStudio** | Live demo | TypeScript | Next.js, Three.js / R3F, WebGPU / WebGL2, Web Audio |
| **AudioSplit** | Live demo | TypeScript, HTML / JS | — |
| **Sonic-Space** | In development | TypeScript | — |
| **LastWave-Desktop** | Fork (source only) | Dart | mpv, WASAPI |
| **PixelMusicApp** | Fork (source only) | Kotlin | — |

---

## Tech stack

- **Vanilla HTML / CSS / JavaScript** — zero build step, zero framework, zero bundler
- **Canvas 2D API** — all interactive visuals
- **GitHub REST API v3** — live project and contributor data
- **Bricolage Grotesque + DM Mono** — via Google Fonts
- **Vercel** — hosting

---

## Configuration

Open `portfolio.html` and set the two constants near the top of the `<script>` block:

```js
const SITE_URL = "https://umang-portfolio-three.vercel.app"; // your production domain
const GH_USER  = "Umangnamdeo";                              // GitHub username to sync from
```

Setting `SITE_URL` automatically updates the canonical `<link>`, `og:url`, and JSON-LD structured data.

---

## Running locally

No build step required. Open the file directly in any modern browser:

```bash
# Option A — just open the file
open portfolio.html

# Option B — serve over HTTP (avoids some browser file:// restrictions)
npx serve .
# or
python3 -m http.server 8080
```

> **Note:** The GitHub API sync works over HTTP/HTTPS. When opened as a `file://` URL, browsers may block the API request; use a local server for full sync behaviour.

---

## Deploying to Vercel

1. Push `portfolio.html` (rename to `index.html`) to a GitHub repository.
2. Import the repository at [vercel.com/new](https://vercel.com/new).
3. Framework preset: **Other**. No build command or output directory needed.
4. Deploy. Vercel serves `index.html` at the root automatically.

---

## Project accuracy notes

The site distinguishes between confirmed and reported technology:

- **Solid tags** in project cards = pulled directly from the GitHub API (`language`, `topics`).
- **Dashed tags** = reported from earlier research; not re-verified in the source code.
- Fork projects (LastWave-Desktop, PixelMusicApp) are clearly attributed to their upstream authors. They are not presented as original work.
- Sonic-Space is marked **In development**; its description states goals, not shipped functionality.

---

## Contact

| | |
|---|---|
| Email | umangwebwork24@gmail.com |
| GitHub | github.com/Umangnamdeo |
| LinkedIn | linkedin.com/in/umang-namdeo-31a2b3428 |
| Instagram | instagram.com/umang_namdeo |

---

© 2026 Umang Namdeo
