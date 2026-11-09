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
