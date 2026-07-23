# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Marketing website for Hyperformance Media, a Delhi-based digital marketing agency (SEO, web dev, CRM, e-commerce, AI modelling, social, performance marketing). Built with Astro + Tailwind CSS v4. Static-first, minimal client JS.

Read `PRODUCT.md` and `DESIGN.md` before making copy or visual-design decisions — they define positioning, target audience, anti-references, and the full design token system (colors, type scale, component specs, do's/don'ts). Don't restate their contents here; consult them directly.

## Commands

```
npm run dev              # dev server (foreground)
astro dev --background   # dev server in background — preferred, see below
astro dev stop           # stop background dev server
astro dev status         # check background dev server status
astro dev logs           # tail background dev server logs
npm run build             # production build to ./dist/
npm run preview           # preview production build locally
npm run astro check       # type-check .astro files
```

There is no test suite and no lint script configured. `astro check` is the only correctness check available.

### Development

When starting the dev server, use background mode (`astro dev --background`) and manage it with `astro dev stop` / `astro dev status` / `astro dev logs` rather than a foreground process.

## Architecture

- **Astro v7, file-based routing** — every route is a file under `src/pages/*.astro` (`index`, `about`, `services`, `contact`, `privacy`, `terms`, `404`). No content collections, no CMS, no server framework — pages are static Astro components with inline props/data.
- **`src/layouts/BaseLayout.astro`** is the single shared shell: fonts, `global.css`, `<head>` SEO tags (title/description/canonical/OG/Twitter), and per-page JSON-LD structured data (`schema` prop, defaults to `MarketingAgency` schema.org type). It also renders `Navbar`, `Footer`, `FloatingContactActions` around the page `<slot>`, and owns all site-wide vanilla-JS behavior added inline in `<script>` tags at the bottom:
  - Scroll-reveal: `IntersectionObserver` toggles `.is-visible` on any `[data-reveal]` element (variants: `fade`/`scale`/`left`/`right`, stagger via `[data-reveal-delay="1..6"]`).
  - Animated count-up on `[data-count]` elements (`data-suffix`, `data-prefix`, `data-decimals` attributes).
  - Pointer-tilt effect on `[data-tilt-card]` / `[data-tilt-layer]` elements.
  - All three respect `prefers-reduced-motion`.
  - When adding a new interactive/animated section, reuse these existing data-attribute hooks rather than writing new bespoke JS — most sections already have what they need available site-wide.
- **Components** (`src/components/*.astro`) are one-per-section (`Hero`, `Mission`, `Stats`, `Process`, `WhyUs`, `Testimonials`, `FinalCta`, `ServicesNetwork`, `FloatingContactActions`) plus shared chrome (`Navbar`, `Footer`). Pages compose these directly; there's no shared "page section" abstraction beyond the components themselves.
- **Styling**: Tailwind v4 via `@tailwindcss/vite`, configured entirely in CSS (`src/styles/global.css`) using `@theme` — there is no `tailwind.config.js`. Design tokens (colors, font families, type scale, radii, shadows) are defined as CSS custom properties there and consumed as Tailwind utilities (e.g. `text-h1`, `bg-surface`, `rounded-card`, `shadow-card`). Light/dark values are set via `:root` / `.dark` blocks — note `BaseLayout.astro` currently defaults new visitors to dark theme via an inline script, which is worth double-checking against `DESIGN.md`'s "don't use dark mode" guidance before assuming either is authoritative.
- **Fonts**: self-hosted via `@fontsource-variable/*` packages, imported directly in `BaseLayout.astro` (Bricolage Grotesque for headings, Manrope for body — Inter and Plus Jakarta Sans packages are also installed but not currently wired in).
- **SEO infra**: `@astrojs/sitemap` integration (configured in `astro.config.mjs` with `site: 'https://hyperformancemedia.in'`), static `public/robots.txt` and `public/llms.txt`, per-page canonical/OG/JSON-LD via `BaseLayout` props.
- **Images**: static assets live in `src/assets/` (processed by Astro's image pipeline when imported) vs `public/` (served as-is, unoptimized) — check which one an existing similar asset uses before adding a new one.
