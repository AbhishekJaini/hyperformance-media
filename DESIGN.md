---
name: Hyperformance Media
description: AI-powered digital marketing agency — bold, tech-forward, trust-building
colors:
  primary: "#2563eb"
  primary-dark: "#1d4ed8"
  primary-light: "#3b82f6"
  background: "#ffffff"
  surface: "#f8f9fb"
  text-primary: "#0f172a"
  text-secondary: "#64748b"
  border: "#e2e8f0"
typography:
  display:
    fontFamily: "Plus Jakarta Sans Variable, Plus Jakarta Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "3.5rem"
    fontWeight: 700
    lineHeight: 1.07
    letterSpacing: "normal"
  headline:
    fontFamily: "Plus Jakarta Sans Variable, Plus Jakarta Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "2.75rem"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "normal"
  title:
    fontFamily: "Plus Jakarta Sans Variable, Plus Jakarta Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: "normal"
  body:
    fontFamily: "Inter Variable, Inter, ui-sans-serif, system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  body-lg:
    fontFamily: "Inter Variable, Inter, ui-sans-serif, system-ui, -apple-system, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Inter Variable, Inter, ui-sans-serif, system-ui, -apple-system, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: "0.05em"
rounded:
  card: "0.75rem"
  button: "0.5rem"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
  3xl: "80px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "{rounded.button}"
    padding: "14px 28px"
    typography: "{typography.body}"
  button-primary-hover:
    backgroundColor: "{colors.primary-dark}"
  button-secondary:
    backgroundColor: "{colors.background}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.button}"
    padding: "14px 28px"
    typography: "{typography.body}"
  button-secondary-hover:
    backgroundColor: "{colors.background}"
    textColor: "{colors.primary}"
  card:
    backgroundColor: "{colors.background}"
    rounded: "{rounded.card}"
    padding: "32px"
  card-surface:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.card}"
    padding: "32px"
  input:
    backgroundColor: "{colors.background}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.button}"
    padding: "12px 16px"
    typography: "{typography.body}"
  input-focus:
    backgroundColor: "{colors.background}"
    textColor: "{colors.text-primary}"
---

# Design System: Hyperformance Media

## 1. Overview

**Creative North Star: "The Precision Engine"**

This is a marketing website for an AI-powered digital marketing agency serving small and medium businesses across India. The design needs to do one thing: make a skeptical SMB owner feel "these people know what they're doing, and they can do it for me." That means confidence through clarity, not flash. Every element is purposeful — the visual equivalent of a well-tuned engine where every part does exactly what it should, nothing more.

The system is built on a single blue accent (`#2563eb`) against white and near-white surfaces, with Plus Jakarta Sans carrying headlines (geometric, confident) and Inter carrying body (neutral, legible). Restraint is the point: one accent color, two fonts, two surface tones, one shadow family. The boldness lives in the typography scale and the directness of the copy, not in visual complexity. Sections alternate between white and `#f8f9fb` to create rhythm without color noise.

What this system explicitly rejects: stock-photo agency templates with blue gradient heroes, "we are passionate" copy, trust badges, identical 4-card service grids, and any layout that could be guessed as "agency site" from the structure alone. The personality is bold and tech-forward, but the delivery is quiet — trust and relief, not anxiety or hype.

**Key Characteristics:**
- Single-accent palette (blue `#2563eb` on white/surface neutrals)
- Two-font system (Plus Jakarta Sans display + Inter body)
- Restrained radius (12px cards, 8px buttons — not bubbly)
- Low-opacity ambient shadows (depth without heaviness)
- Alternating section backgrounds for rhythm
- Direct, concrete copy — numbers over adjectives

## 2. Colors

A single-accent system: one professional blue carries all brand energy against a white-to-near-white neutral surface range. No secondary or tertiary accents — the blue's rarity is what makes it land.

### Primary
- **Professional Blue** (`#2563eb`): The single brand accent. Used on primary CTAs, links, active states, icon backgrounds (`primary/10` tint), and the final CTA band. Appears on ≤15% of any given screen — its restraint is the point.
- **Blue Deep** (`#1d4ed8`): Hover and pressed states for primary buttons. Slightly darker, same hue.
- **Blue Light** (`#3b82f6`): Available for subtle highlights and focus rings; used sparingly.

### Neutral
- **White** (`#ffffff`): Default page background. The clean canvas.
- **Surface** (`#f8f9fb`): Very light cool-neutral for alternating sections and card backgrounds on white pages. Barely tinted — reads as "off-white" not "gray."
- **Ink** (`#0f172a`): Near-black for all headings and primary text. Slate undertone, not pure black.
- **Slate** (`#64748b`): Medium gray for body copy, subtext, and secondary labels. Hits 4.5:1 contrast against white.
- **Border** (`#e2e8f0`): Light gray for dividers, card borders, input strokes. Visible but never loud.

### Named Rules
**The One Accent Rule.** Blue `#2563eb` is the only saturated color in the system. No purples, no greens, no gradients, no warm accents. If something needs to stand out, it uses blue or it uses weight/size — never a second hue.

**The Surface Alternation Rule.** Sections alternate between white (`#ffffff`) and surface (`#f8f9fb`) to create visual rhythm. Never two surface sections in a row; never three white sections in a row without a break.

## 3. Typography

**Display Font:** Plus Jakarta Sans Variable (with Plus Jakarta Sans, ui-sans-serif, system-ui fallback)
**Body Font:** Inter Variable (with Inter, ui-sans-serif, system-ui, -apple-system fallback)

**Character:** Plus Jakarta Sans is geometric and confident — modern without being cold, friendly without being casual. Inter is the neutral workhorse: legible at every size, invisible as a personality, which is exactly what body text should be. The pairing works because they're different enough (geometric display vs. neo-grotesque body) to create hierarchy, but both are sans-serif so the system feels unified.

### Hierarchy
- **Display / H1** (700, 3.5rem / 56px, line-height 1.07): Hero headline only. One per page. `text-wrap: balance` for even line lengths.
- **Headline / H2** (700, 2.75rem / 44px, line-height 1.1): Section headlines. The workhorse heading. `text-wrap: balance`.
- **Title / H4** (600, 1.5rem / 24px, line-height 1.25): Card titles, subsection headers, service names.
- **Body Large** (400, 1.125rem / 18px, line-height 1.6): Lead paragraphs, hero subtext. Max line length 65–75ch.
- **Body** (400, 1rem / 16px, line-height 1.6): Default body copy. Max line length 65–75ch.
- **Label** (500, 0.875rem / 14px, line-height 1.5): Captions, meta, eyebrow labels (uppercase, tracked +0.05em when used as eyebrow).

### Named Rules
**The Two-Font Rule.** Plus Jakarta Sans for headings, Inter for everything else. No exceptions, no third family. If a special treatment is needed, use weight or size within the existing families.

**The Eyebrow Restraint Rule.** Uppercase tracked eyebrows (`text-body-sm font-medium uppercase tracking-wider text-primary`) are used on section headers, but not on every section — vary the cadence so they don't become the saturated AI scaffold. Some sections lead with the headline directly.

## 4. Elevation

This system uses low-opacity ambient shadows — depth without heaviness. Shadows are subtle enough that they read as "this is a card" not "this is floating." The shadow family uses the ink color (`#0f172a`) at very low opacity, so it feels like a natural shadow rather than a black drop.

### Shadow Vocabulary
- **Card Rest** (`0 1px 3px 0 rgb(15 23 42 / 0.06), 0 1px 2px -1px rgb(15 23 42 / 0.06)`): Default card shadow. Barely visible — just enough to separate the card from the surface.
- **Card Hover** (`0 4px 12px -2px rgb(15 23 42 / 0.08), 0 2px 6px -2px rgb(15 23 42 / 0.06)`): Elevated hover state. Slightly more lift, still restrained.

### Named Rules
**The Flat-By-Default Rule.** Cards are flat at rest with the card-rest shadow. The hover shadow appears only as a response to interaction. Never apply card-hover to a non-interactive element.

## 5. Components

### Buttons
- **Shape:** 8px radius (`rounded-button`), inline-flex, items-center, justify-center
- **Primary:** Blue `#2563eb` background, white text, 14px 28px padding, `text-body` weight 500. Hover: `#1d4ed8`. Transition: `transition-colors`.
- **Secondary / Ghost:** White `#ffffff` background, 1px border `#e2e8f0`, ink text `#0f172a`. Hover: border → blue, text → blue. Same padding and radius as primary.
- **Full-width (mobile):** `w-full` on mobile, `sm:w-auto` on desktop. Used in hero CTAs and mobile nav.

### Cards
- **Corner Style:** 12px radius (`rounded-card`)
- **Background:** White `#ffffff` (on surface pages) or surface `#f8f9fb` (on white pages — rare)
- **Shadow Strategy:** Card Rest at default, Card Hover on interactive hover. See Elevation.
- **Border:** 1px `#e2e8f0` — always present, never removed. The border + shadow together create the card edge.
- **Internal Padding:** 32px (`p-8`) standard. 24px (`p-6`) for compact variants.

### Inputs / Fields
- **Style:** 1px border `#e2e8f0`, white background, 8px radius, 12px 16px padding, `text-body` size.
- **Focus:** Border → blue `#2563eb`, ring → `ring-2 ring-primary/20`. Transition: `transition-colors`.
- **Placeholder:** `text-text-secondary/60` — slightly muted but still legible.
- **Labels:** `text-body-sm font-medium text-text-primary`, 6px margin-bottom.

### Navigation
- **Sticky header:** White background, 1px bottom border `#e2e8f0`, `z-50`.
- **Logo:** Horizontal lockup image, 40px height (navbar) / 36px (footer), auto width.
- **Desktop links:** `text-body text-text-secondary`, hover → `text-text-primary`. 32px gap between items.
- **Desktop CTA:** Primary button, 20px padding-y, 20px padding-x.
- **Mobile:** Hamburger toggle (24px icon), slide-down menu with full-width links and CTA. Menu hidden by default, toggled via JS.

### Eyebrow / Section Label
- **Style:** `inline-flex items-center rounded-full` pill, `text-body-sm font-medium uppercase tracking-wider text-primary`.
- **Background:** `bg-surface` on white sections, `bg-background` on surface sections (inverted).
- **Padding:** 6px 16px (`px-4 py-1.5`).
- **Usage:** Not on every section — vary the cadence. See Eyebrow Restraint Rule.

### Stat Block
- **Layout:** Grid, 2-col mobile, 3-col small tablet, 5-col desktop.
- **Value:** `text-4xl font-bold text-white md:text-h2` on primary background.
- **Label:** `text-body text-white/80`, 8px margin-top.
- **Background:** Primary blue `#2563eb` — the one section where blue drenches the surface.

## 6. Do's and Don'ts

### Do:
- **Do** use blue `#2563eb` as the single accent for all interactive elements, links, and brand moments. Its rarity is what makes it land.
- **Do** alternate section backgrounds between white (`#ffffff`) and surface (`#f8f9fb`) for rhythm.
- **Do** use Plus Jakarta Sans for all headings and Inter for all body copy. Weight and size create hierarchy, not font switching.
- **Do** keep body line length at 65–75ch (`max-w-3xl` or `max-w-2xl` on lead paragraphs).
- **Do** use `text-wrap: balance` on h1–h3 for even line lengths.
- **Do** back every claim with a concrete number or example. "We doubled their traffic in 4 months" not "we deliver exceptional results."
- **Do** use low-opacity ambient shadows (`shadow-card`) for depth — never heavy drop shadows.
- **Do** ensure body text hits 4.5:1 contrast against its background. The current `#64748b` on `#ffffff` passes; don't go lighter.

### Don't:
- **Don't** use stock photos of people pointing at laptops, blue gradient heroes, or "we are passionate about what we do" copy. This is the generic agency template look — the #1 anti-reference.
- **Don't** introduce a second accent color. No purples, no greens, no warm accents. Blue or weight/size — never a second hue.
- **Don't** use gradient text (`background-clip: text` with a gradient). Single solid colors only.
- **Don't** put uppercase tracked eyebrows on every section. Vary the cadence so they don't become AI scaffolding.
- **Don't** use border-left or border-right greater than 1px as a colored accent stripe on cards or callouts.
- **Don't** use glassmorphism (blurs, glass cards) decoratively. Rare and purposeful, or nothing.
- **Don't** use identical same-sized cards with icon + heading + text repeated endlessly. Vary the layout when the content varies.
- **Don't** use dark mode for this site. The audience is SMB owners in India — clarity and legibility on bright screens in daylight is the physical scene.
- **Don't** use "passionate," "cutting-edge," "synergistic," "leverage," or any marketing jargon a hundred other agency sites use. Direct, concrete, human.
