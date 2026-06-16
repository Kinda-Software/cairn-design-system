---
version: alpha
name: Cairn
description: Named after the stone trail markers of the Peak District — Cairn guides designers and agents through consistent, purposeful UI decisions. Supports two distinct surface types (App UI and Marketing UI) across multiple products sharing a common foundation with per-product brand colour theming.
colors:
  primary: "#5B6EE1"          # brand-500 — vibrant accent. Rings, 0.5px borders, large display only. Fails AA as white-text bg.
  primary-light: "#818CF8"    # brand-400 — dark-mode interactive + marketing eyebrow
  primary-muted: "#E8EAFF"    # brand-50
  primary-text: "#3A4DC8"     # brand-700 — text on brand-50
  primary-nav: "#1E2660"      # brand-900
  primary-dark-muted: "#1E254A"
  primary-dark-nav: "#0F1330"
  brand-solid: "#3A4DC8"      # SEMANTIC: solid-fill / brand-text stop = brand-700 (light). ≥5.8:1 with white, all products. Dark mode resolves to brand-400.
  brand-contrast: "#FFFFFF"   # SEMANTIC: text/icon colour on brand-solid (ink in dark mode)
  neutral: "#F5F5F4"
  neutral-raised: "#FFFFFF"
  neutral-border: "#E5E5E3"
  neutral-mid: "#78716C"      # decorative/icon stop ONLY — 4.4:1 on canvas, fails AA as body text
  neutral-text: "#6B6560"     # neutral-550 — secondary TEXT stop. 5.3:1 on canvas / 5.7:1 on white
  neutral-strong: "#1C1917"
  ink: "#18181A"
  success: "#16A269"
  success-muted: "#D1FAE5"
  success-text: "#065F46"
  error: "#E05B40"            # soft/icon ember — fails white text, never a solid-button fill
  error-solid: "#A8341C"      # solid destructive fill — 6.6:1 with white
  error-muted: "#FEF0ED"
  error-text: "#991B1B"       # text on error-muted/error-badge (≥6.8:1) and subtle destructive button label
  error-badge: "#FEE2E2"
  warning-muted: "#FEF3C7"
  warning-text: "#92400E"
  mkt-canvas: "#0D0D12"
  mkt-surface: "#16161E"
  mkt-surface-raised: "#1E1E28"
# App scale — anchored at 14px body, modular ratio ≈ 1.2 (minor third).
# Marketing scale — anchored at 16px body, modular ratio ≈ 1.25 (major third).
typography:
  display:
    fontFamily: Space Grotesk
    fontSize: 29px       # 14 × 1.2⁴
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.03em
  heading-lg:
    fontFamily: Space Grotesk
    fontSize: 24px       # 14 × 1.2³
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.022em
  heading-md:
    fontFamily: Space Grotesk
    fontSize: 20px       # 14 × 1.2²
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: -0.017em
  heading-sm:
    fontFamily: Space Grotesk
    fontSize: 17px       # 14 × 1.2
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: -0.011em
  label:
    fontFamily: Space Grotesk
    fontSize: 14px       # = body, weight-bumped
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: 0em
  body-md:
    fontFamily: Space Grotesk
    fontSize: 14px       # ANCHOR
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0em
  body-sm:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: 0em
  caption:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0.005em
  mono:
    fontFamily: Space Mono
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: 0em
  mkt-display:
    fontFamily: Space Grotesk
    fontSize: 76px       # 16 × 1.25⁷
    fontWeight: 600
    lineHeight: 1.0
    letterSpacing: -0.04em
  mkt-heading:
    fontFamily: Space Grotesk
    fontSize: 49px       # 16 × 1.25⁵
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: -0.03em
  mkt-subheading:
    fontFamily: Space Grotesk
    fontSize: 25px       # 16 × 1.25²
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.018em
  mkt-body-lg:
    fontFamily: Space Grotesk
    fontSize: 20px       # 16 × 1.25 — lead paragraph
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: -0.005em
  mkt-body:
    fontFamily: Space Grotesk
    fontSize: 16px       # ANCHOR
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: 0em
  mkt-eyebrow:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.09em
  mkt-caption:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0em
rounded:
  sm: 4px
  md: 8px
  lg: 12px
  xl: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  sm-md: 12px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
  gutter-mobile: 24px
  gutter-desktop: 40px
  section-mobile: 48px
  section-desktop: 80px
iconography:
  library: Phosphor Icons
  license: MIT
  baseGrid: 16px               # icons drawn on a 16px grid — scale by 4px steps
  defaultWeight: regular
  sizes:
    inline: 16px               # within body/caption text, status dots, dense tables
    ui: 20px                   # DEFAULT — buttons, toolbar, table actions, nav items
    emphasis: 24px             # app top bar, section headers, primary nav
    feature: 28px              # marketing feature-card glyph (inside 32px container)
  weights:
    regular: "default — app content, marketing inline, most nav"
    bold: "small sizes (≤16px) and the dark sidebar where regular reads thin"
    fill: "active / selected states only — pairs with nav-item-active"
    duotone: "marketing feature-card glyphs + app empty/onboarding moments — brand-tinted"
  color:
    decorative: "{colors.neutral-mid}"       # #78716C — icon/decorative stop, never informational
    interactive: "{colors.ink}"              # actionable icon at rest (light content area)
    active: "{colors.brand-solid}"           # selected interactive icon in light content
    sidebar-rest: "rgba(255,255,255,0.65)"   # matches nav-item-rest label
    sidebar-active: "{colors.neutral-raised}"# full-opacity white, matches nav-item-active
    status: "Sage (success) / Ember (error) — never the brand colour"
    duotone-foreground: "{colors.primary-light}"  # #818CF8 on dark; brand-solid on light
  duotoneSecondaryOpacity: 0.20  # Phosphor duotone back layer — auto-tints from foreground
components:
  button-primary:
    backgroundColor: "{colors.brand-solid}"     # brand-700, not brand-500 — white label needs ≥4.5:1
    textColor: "{colors.brand-contrast}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-primary-hover:
    backgroundColor: "brand-solid darkened ~6% L (--brand-solid-hover)"
    textColor: "{colors.brand-contrast}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-ghost:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.neutral-text}"           # neutral-550 — neutral-mid fails (4.4:1) on the stone fill
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-destructive:                            # subtle/soft destructive
    backgroundColor: "{colors.error-muted}"
    textColor: "{colors.error-text}"             # was error (#E05B40, 3.3:1 — failed); error-text passes
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-destructive-solid:                      # filled destructive (white label)
    backgroundColor: "{colors.error-solid}"      # ember-solid, 6.6:1 with white
    textColor: "{colors.neutral-raised}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  badge:
    typography: "{typography.caption}"
    rounded: "{rounded.full}"
    padding: 3px 10px
  badge-active:
    backgroundColor: "{colors.primary-muted}"
    textColor: "{colors.primary-text}"
  badge-success:
    backgroundColor: "{colors.success-muted}"
    textColor: "{colors.success-text}"
  badge-error:
    backgroundColor: "{colors.error-badge}"
    textColor: "{colors.error-text}"
  badge-warning:
    backgroundColor: "{colors.warning-muted}"
    textColor: "{colors.warning-text}"
  badge-neutral:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.neutral-text}"           # neutral-550 for AA on the stone fill
  input-default:
    backgroundColor: "{colors.neutral-raised}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 12px
  input-focus:
    backgroundColor: "{colors.neutral-raised}"
    textColor: "{colors.ink}"
  card:
    backgroundColor: "{colors.neutral-raised}"
    rounded: "{rounded.lg}"
    padding: 16px 20px
  table-header:
    textColor: "{colors.neutral-text}"           # neutral-550 — passes on stone canvas as well as white cards
    typography: "{typography.caption}"
    height: 36px
    padding: 0px 12px
  table-row:
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
    height: 44px
    padding: 0px 12px
  table-row-compact:
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
    height: 32px
    padding: 0px 12px
  table-row-hover:
    backgroundColor: "{colors.neutral}"
  nav-sidebar:
    backgroundColor: "{colors.primary-dark-nav}"
    width: 192px
  nav-item-rest:
    textColor: "rgba(255,255,255,0.65)"
    rounded: "{rounded.md}"
    padding: 6px 8px
  nav-item-active:
    backgroundColor: "rgba(91,110,225,0.15)"
    textColor: "{colors.neutral-raised}"
    rounded: "{rounded.md}"
    padding: 6px 8px
  nav-item-hover:
    backgroundColor: "rgba(255,255,255,0.06)"
    textColor: "rgba(255,255,255,0.85)"
  mkt-button-primary:
    backgroundColor: "{colors.brand-solid}"      # AA-safe fill; CTA glow shadow supplies luminosity
    textColor: "{colors.brand-contrast}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 40px
    padding: 11px 22px
  mkt-button-primary-large:
    backgroundColor: "{colors.brand-solid}"
    textColor: "{colors.brand-contrast}"
    rounded: "{rounded.md}"
    height: 50px
    padding: 14px 28px
  mkt-button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.neutral-raised}"
    rounded: "{rounded.md}"
    height: 40px
    padding: 11px 22px
  mkt-button-text:
    backgroundColor: "transparent"
    textColor: "{colors.primary-light}"
    height: 40px
    padding: 11px 16px
  mkt-feature-card:
    backgroundColor: "{colors.mkt-surface}"
    rounded: "{rounded.lg}"
    padding: 18px
  mkt-pricing-card:
    backgroundColor: "{colors.mkt-surface}"
    rounded: "{rounded.lg}"
    padding: 20px
  mkt-pricing-card-featured:
    backgroundColor: "{colors.mkt-surface}"
    rounded: "{rounded.lg}"
    padding: 20px
  mkt-nav:
    backgroundColor: "transparent"
    height: 52px
  mkt-nav-scrolled:
    backgroundColor: "{colors.mkt-canvas}"
---

## Overview

Cairn is named after the stone trail markers used by walkers in the Peak District — stacked stones placed at path junctions and summits to guide you through uncertain terrain without demanding attention. This system works the same way: it guides consistent UI decisions across products and surfaces while staying out of the way of the work itself.

Cairn is a multi-product SaaS design system built around restraint and purposefulness. It supports two fundamentally distinct surface types — **App UI** and **Marketing UI** — that share a typographic and structural foundation but follow different rules for how design elements are deployed.

## Component Foundation

**shadcn-svelte is the default component set for all Kinda products.** Cairn does not define bespoke components from scratch — it defines the tokens, constraints, and usage guidelines that are applied on top of shadcn-svelte's component library.

This means:

- **shadcn-svelte provides the component implementations** — buttons, inputs, badges, cards, tables, dialogs, and so on. You own the files (shadcn copies them into your repo), so customisation is direct rather than via overrides.
- **Cairn provides the CSS tokens** that map to shadcn's variable layer (`--background`, `--primary`, `--border`, etc.), replacing shadcn's default palette with Cairn's warm stone neutrals and brand colours.
- **Cairn provides the usage guidelines** — which variants to use in which contexts, what constraints apply (no gradients on buttons, no zebra stripes on tables, one primary action per view), and how components behave differently on the App UI versus Marketing surface.
- **Cairn provides the per-product theming model** — the `data-theme` attribute and 7 brand primitive properties that shadcn components inherit automatically.

For setup, token mapping, and component-level override code, see [cairn-shadcn.md](./cairn-shadcn.md). The sections below document the intended behaviour and constraints — the *what* and *why*, not the *how*.

**Typeface:** Space Grotesk (400, 500, 600) for all UI and marketing text. Space Mono (400, 700) exclusively for code, numeric financial tables, and technical identifiers. Both fonts share design DNA — the pairing feels intentional rather than assembled.

**Multi-product architecture:** The system hosts multiple products, each with its own brand colour. All products share the same typography, spacing, radius, motion, and neutral palette. Only the brand colour ramp changes per product. The default product colour is Indigo (Orbit product). Products are themed via a `data-theme` attribute on the root element, which injects 7 brand primitive CSS custom properties that the semantic layer references automatically.

**App UI surface:** Task-based and information-dense. The job is to help users accomplish work efficiently. Brand colour appears only on interactive elements. Stone warm-tinted neutrals carry all surface structure. Personality lives in the font details, nowhere else.

**Marketing surface:** Persuasion-based. The job is to build confidence, communicate value, and drive conversion. A dark canvas (`mkt-canvas`, #0D0D12) is the default — it makes the brand colour read as a light source rather than a tint, which is more emotionally activating. Marketing tokens use the `mkt-` prefix and are additive — they never override app tokens.

## Colors

Cairn uses warm-tinted stone neutrals rather than pure grey — the slight warmth prevents surfaces from feeling clinical. Brand colour is strictly functional: it signals interactivity in the app and acts as a light source in marketing. Only two status colours are defined: Sage (success) and Ember (error/destructive).

- **Primary (#5B6EE1):** Indigo — the default brand colour (Orbit product). brand-500 is the vibrant accent: focus rings, 0.5px borders, large display accents. It is **not** AA-safe behind white text (3.4–4.6:1 across products) so it never fills a button or carries normal-size text. Used exclusively on interactive elements in the app — never decorative.
- **Brand Solid / Brand Contrast (semantic):** The accessible interactive pair every solid fill and brand-coloured text references. `brand-solid` resolves to `brand-700` (#3A4DC8 for Orbit) in light mode and `brand-400` in dark mode; `brand-contrast` is the text/icon colour on top (white in light, ink in dark). Solid fills clear ≥5.8:1 with white on every product. Hover darkens `brand-solid` by ~6% lightness, hue-locked. This is what `--primary` points at — components never hardcode a brand stop for fills.
- **Neutral Text (#6B6560):** Stone-550 — the secondary/tertiary **text** stop (captions, table headers, ghost labels, placeholders, helper text). Reads as subdued while clearing 4.5:1 on both the stone canvas (5.3:1) and white cards (5.7:1). The older neutral-mid (#78716C) only reaches 4.4:1 on the canvas and is now reserved for decorative and icon use, never informational text.
- **Primary Light (#818CF8):** Lighter indigo stop for dark mode interactive elements and as the marketing eyebrow accent colour. On dark surfaces it reads as a light source.
- **Primary Muted (#E8EAFF):** Light tint for badge backgrounds, focus rings, and selected states. Flips to `primary-dark-muted` (#1E254A) in dark mode.
- **Neutral (#F5F5F4):** Stone 50 — the app page canvas. Warm-tinted to avoid the clinical feel of pure grey.
- **Neutral Raised (#FFFFFF):** Card and surface backgrounds in light mode.
- **Neutral Border (#E5E5E3):** All structural borders in the app UI. Always 0.5px weight.
- **Ink (#18181A):** Primary text colour.
- **Success (#16A269) / Success Muted (#D1FAE5):** Status states only. Never used for branding or decoration.
- **Error (#E05B40) / Error Solid (#A8341C) / Error Muted (#FEF0ED):** Destructive actions and error states only. The soft Error tone (#E05B40) is for icons, borders, and the subtle destructive button (paired with `error-text` on `error-muted`); it fails white-text contrast so a **filled** destructive button uses Error Solid (#A8341C, 6.6:1 with white).
- **Marketing Canvas (#0D0D12):** The dark surface for all marketing sections. Always hardcoded — never inherited from the app theme.
- **Marketing Surface (#16161E):** Raised feature cards and panels on the dark canvas.

**Per-product theming:** Each product defines 7 brand CSS custom properties: `--brand-500` (vibrant accent), `--brand-400` (dark mode variant — lighter), `--brand-50` (muted fill), `--brand-700` (text on muted + solid fill), `--brand-900` (nav background), `--brand-dark-muted`, `--brand-dark-nav`. The semantic `brand-solid`/`brand-contrast` pair derives automatically from these (`brand-700`/white in light, `brand-400`/ink in dark) — adding a product needs no extra tokens, but `--brand-700` must be checked for ≥4.5:1 against white since it is now a solid-button fill. Not all brand colours work in all positions — `--brand-dark-nav` in particular must be independently authored per product, not mechanically darkened.

## Typography

Space Grotesk is used across both surfaces. Its double-storey `a`, spurred `G`, curved-tail `t`, and strong numerals give it personality at display sizes while remaining legible at 12px in dense UIs. Space Mono is paired for code and financial figures — both fonts share design DNA, making the pairing feel designed rather than assembled.

**Scale construction:** Both surfaces are built as modular scales from an explicit body anchor. The **app scale is anchored at 14px** with a ratio of ≈1.2 (minor third) — dense and efficient. The **marketing scale is anchored at 16px** with a ratio of ≈1.25 (major third) — more presence and air. Every step is derived from its anchor rather than chosen ad hoc, so the two surfaces stay internally consistent and visibly distinct.

**Weight rule:** 600 is reserved for the largest steps — app `display` (29px) and the marketing `heading`/`display` steps. Space Grotesk 500 is optically heavier than Inter 500, so 500 carries every heading below display and using 600 at smaller sizes produces a heavy, overworked result.

**Tracking rule:** Negative tracking increases with size. App display: −0.03em. Marketing display: −0.04em at 76px (letterforms need maximum compression). Marketing heading: −0.03em at 49px. Body and label tracking is 0; the largest body step (marketing body-lg, 20px) takes a faint −0.005em.

**App scale:** 12px caption → 29px display, anchored at 14px body. Steps: caption 12, body-sm 13, body 14, label 14/500, heading-sm 17, heading-md 20, heading-lg 24, display 29. Tight tracking on headings, neutral on body. Line height 1.6 on body (slightly tighter than default to compensate for Space Grotesk's natural width).

**Marketing scale:** 13px eyebrow → 76px hero, anchored at 16px body. Steps: eyebrow 13, caption 14, body 16, body-lg 20 (lead paragraph), subheading 25, heading 49, display 76. Eyebrows use uppercase with wide positive tracking (+0.09em) in `primary-light` colour — never white, which would compete with the headline for first read. The scale is deliberately larger than the app UI — marketing pages reward confidence.

**Animation rule:** Marketing headlines at the heading step (49px) and above use fade-only animation transitions. Never use translateY on large text — moving text at that scale looks like a rendering error.

## Iconography

**Library:** [Phosphor Icons](https://phosphoricons.com) — MIT licensed, free for commercial use, ~1,250 icons. Phosphor is chosen for two reasons. It is built on a strict geometric grid of circular and square base forms, which echoes Space Grotesk's geometric-grotesque construction without competing with it. And it ships six weights (Thin, Light, Regular, Bold, Fill, Duotone) from a single family, so icon weight can be tuned per surface rather than locked to one stroke — the same flexibility Cairn relies on to hold up across a light content area and the always-dark sidebar. Use one library only; never mix Phosphor with another icon set, as differing grids and stroke logic read as inconsistency even when individual icons are clean.

**Weight rule (mirrors the type weight rule):** Regular is the default everywhere. Step up deliberately, not decoratively. Use **Bold** at small sizes (≤16px) and on the dark sidebar, where a regular-weight line can read thin against #0F1330 — this is the answer to "bold enough for both modes." Reserve **Fill** for active and selected states only, where it pairs with `nav-item-active` to signal the current location. Just as 600 is reserved for the largest type steps, Bold and Fill are reserved for specific roles — blanket-bolding every icon produces the same heavy, overworked result as over-using 600.

**Sizing:** Icons follow the 4px grid. 20px is the default UI size (buttons, toolbar actions, table action menus, nav items). 16px is for inline use within body or caption text and dense tables. 24px is for the app top bar and section headers. An icon paired with text aligns to the text's optical centre, not its baseline. Don't scale a single icon to an off-grid size to fill space — pick the next grid step or adjust the container.

**Colour in the app:** Decorative and informational-support icons use `neutral-mid` (#78716C) — this is the decorative/icon stop and must never carry meaning that text doesn't also carry, since it only reaches 4.4:1. Genuinely interactive icons (clickable, tappable) take `ink` at rest and may use `brand-solid` when active or selected — this respects the core app rule that **brand colour signals interactivity and nothing else**. Status icons use the Sage and Ember families per state, never the brand colour. In the dark sidebar, icons inherit the nav item's treatment: 65%-white at rest, full-opacity white when active. As non-text UI elements, icons must clear 3:1 against their background; any icon that is the only label for a control needs an accessible name (`aria-label`).

**Duotone and the brand colour:** Duotone is Phosphor's two-layer weight — a full-strength foreground path plus a back layer at 20% opacity that tints automatically from the foreground colour. Set the foreground to a brand stop and the icon reads as a single brand-coloured glyph with a soft tonal fill, no second colour to manage. This is purpose-built for the **marketing feature cards**, whose 32px containers already specify a brand-tinted background and low-opacity brand border: a duotone glyph in `primary-light` (#818CF8) sits inside that container and glows as a light source on the dark canvas, exactly the effect the marketing surface is reaching for. Duotone is also welcome at larger sizes in **app empty states and onboarding** — moments where a single symbolic icon is the focal point and a brand tint reinforces the conversion-to-app handoff thread. Two constraints: do not scatter duotone through dense, working app UI — at 16–20px the back layer muddies and it fights the brand-equals-interactive rule; and when duotone carries the brand colour on a marketing surface, verify the foreground stop clears 3:1 against the card background as a non-text element (`primary-light` on `mkt-surface` passes; a darker brand stop may not).

## Layout

The layout uses a 4px base spacing unit. All spacing values are multiples of 4. Page gutters: 24px mobile / 40px desktop for app surfaces. Marketing sections use 80px vertical padding desktop / 48px mobile, maintaining generous breathing room and a strict one-idea-per-section discipline.

**App layout model:** Fixed sidebar (192px) plus fluid content area. Top navs are not used in the app — they force all products to share horizontal space and overflow as features grow. The sidebar scales vertically without compression and creates clear spatial separation between navigation (left, always dark) and content (right, mode-dependent).

**Marketing layout model:** Centred max-width content with full-bleed dark section backgrounds. Three reusable section patterns: (1) Hero — centred, full-width, eyebrow → headline → body → CTA pair. (2) Feature split — text one side, UI mockup the other, alternating. (3) Social proof — logo bar plus stat trio with section dividers.

**App top bar:** 44px height, white background in light mode, `neutral-border` bottom border. Shows page title left, page-level actions right. Does not repeat sidebar navigation.

## Elevation & Depth

Elevation is expressed through border weight and background contrast — never box shadows in the app UI.

- **Default border:** `0.5px solid neutral-border` — all cards, inputs, table rows
- **Emphasis border:** `0.5px solid` (slightly stronger) — hover states, focus context
- **Featured item:** `1px solid primary` — the only exception to the 0.5px rule. Used for featured pricing cards and comparison highlights. 1px has enough optical weight to differentiate from siblings at card scale without filling the background.
- **App shadows:** Never used
- **Marketing CTA glow:** `box-shadow: 0 0 24px rgba(91,110,225,0.25)` permitted on primary CTA buttons on the dark canvas only — functions as an interactivity signal, not decoration

**Dark mode surface hierarchy inverts:** Light mode — page is lighter (stone-50), cards are lightest (white). Dark mode — page is darkest (ink-950), cards are lighter (ink-900). Same hierarchy logic, opposite direction.

## Shapes

Each radius value maps to a specific element category. Mixing radius scales within the same view is not permitted.

- **sm (4px):** Chips, inline tags, checkbox corners, small interactive elements
- **md (8px):** Inputs, buttons, select controls, table action menus
- **lg (12px):** Cards, feature panels, sidebar nav items, modal outer containers
- **xl (16px):** Modal inner containers, sheets, large overlays
- **full (9999px):** Badges, pills, avatars, toggle switches, "most popular" pricing label

No rounded corners on single-sided borders — if using a left or top accent border, `border-radius: 0` applies. Rounded corners only work with full borders on all sides.

## Components

The following guidelines apply to the shadcn-svelte components used in all Kinda products. Each entry describes the Cairn constraints and usage rules — the shadcn component files handle the implementation, and `app.css` handles the token values. Where a component needs class additions or variant changes beyond the default token mapping, those are documented in [cairn-shadcn.md](./cairn-shadcn.md).

**Button hierarchy:** One primary button per view. The primary button fills with `brand-solid` (the brand-700 stop) and white `brand-contrast` text — no tints or gradients. brand-500 is reserved for the focus ring and is never the fill, because white text on brand-500 fails AA (3.4–4.6:1) while brand-solid clears ≥5.8:1. Secondary for alternative actions alongside primary. Ghost for tertiary and toolbar actions, using `neutral-text` labels (not the lighter neutral-mid, which fails on the stone fill). Destructive comes in two forms: the subtle button pairs `error-text` on `error-muted`, and the filled button uses `error-solid` with white. Both use the Ember family — never a red variant of the brand colour.

In the marketing nav, "Sign in" is always a plain text link, never a button. It is for returning users who know what they want and must not compete visually with the primary conversion CTA.

**Badges:** Pill shape only (`rounded.full`). Colour encodes meaning: `badge-active` uses brand colour, `badge-success` uses Sage, `badge-error` uses Ember, `badge-warning` uses amber tint, `badge-neutral` uses stone. Never use brand colour for neutral or archived states.

**Form inputs:** Height 36px. Focus ring: `box-shadow: 0 0 0 3px rgba(91,110,225,0.12)` plus `brand-500` border colour (the ring is a non-text UI element, so the vibrant stop is fine here at ≥3:1). Error state: `error` border plus `error-muted` background, with `error-text` for any inline message. Labels are always visible above the input — no floating labels.

**Data tables:** No zebra stripes — use hover highlight (`table-row-hover`) only. Alternating row colours fragment attention horizontally. Header cells use uppercase 11px tracking at +0.06em so they recede and the eye lands on data. All numeric columns must be right-aligned with `font-variant-numeric: tabular-nums`. Financial figures use `mono` typography for strict column alignment. Total rows use a slightly heavier border (`1px solid`) and `body-md` 500 weight. Density: `table-row` (44px) default, `table-row-compact` (32px) available.

**App sidebar nav:** Always dark (#0F1330) regardless of light/dark mode. Structure top to bottom: product switcher (product icon + wordmark + chevron — opens product panel) → optional section labels (11px/500/uppercase/50%-white — decorative only, never convey critical navigation state) → nav items → user identity footer. `nav-item-active` uses `rgba(brand, 0.15)` fill, full white label, full opacity icon. Product switcher is the multi-product entry point — clicking reveals a panel listing all accessible products.

**Marketing nav:** `mkt-nav` is transparent at page top. `mkt-nav-scrolled` applies `mkt-canvas` background and a `rgba(255,255,255,0.10)` bottom border on scroll (transition: 200ms ease, position: sticky). Signed-out right side: "Sign in" text link (55%-white) → primary CTA (32px height). Signed-in right side: "Go to app →" in `primary-light` + thin divider + avatar. "Go to app" uses `primary-light` not white — white would compete with the active nav link and wordmark.

**Marketing feature cards (`mkt-feature-card`):** Small 32×32px icon container with brand-tinted background and low-opacity brand border. Symbolic, not illustrative — scales across products without bespoke artwork. Title uses `body-md` 500 weight in white (`--foreground`). Body copy uses `body-sm` at `--muted-foreground` — a solid, WCAG 2.2 AA-guaranteed cool-neutral token (`oklch(0.7400 0.0040 275)`) that achieves ≥ 7:1 contrast on all three marketing surface levels. Never substitute a raw white-opacity value for body copy: the effective contrast of opacity-based text varies by surface, and values below 60% cannot guarantee AA compliance on the raised card background.

**Marketing pricing cards:** Standard uses `mkt-pricing-card`. Featured uses `mkt-pricing-card-featured` with `1px solid primary` border override. Never fill the featured card with the brand colour — a colour-filled background reads as "selected" not "recommended" and reduces legibility of the feature list. "Most popular" pill (`rounded.full`, `primary` background, white text) is positioned above the card's top edge.

**The marketing-to-app handoff:** When a user converts (clicks "Start free trial"), the dark sidebar appears immediately as the visual anchor — it signals "you are now in the product." First app load shows an onboarding checklist rather than an empty dashboard, preventing the jarring emptiness after a high-energy marketing conversion. The brand colour (`primary`) is the continuous visual thread: it appears in the marketing CTA button, then immediately in the app sidebar icon and the first active checklist item.

## Do's and Don'ts

- Do use brand colour only on interactive elements in the app UI — if it is not tappable or clickable, it should not use the brand colour
- Do keep one primary CTA per section or view — multiple primary buttons destroy visual hierarchy
- Don't use zebra stripes on data tables — use `table-row-hover` highlight only
- Do use the `mkt-` token prefix for all marketing-specific values — marketing tokens must never override app semantic tokens
- Don't apply the marketing dark canvas to app UI surfaces — the two surfaces must remain visually and structurally distinct
- Do use 600 font weight only at 22px and above — Space Grotesk 500 is already optically heavy at smaller sizes
- Don't use status colours (success, error) for branding or decoration — they communicate system state only
- Do use stone neutral tokens (warm-tinted) for all app surfaces — never substitute pure grey (#f5f5f5)
- Don't use box shadows in the app UI — elevation is expressed through border weight and background contrast
- Do author each product's `--brand-dark-nav` token independently — do not mechanically darken the brand colour
- Don't animate marketing headlines (48px+) with translateY — use opacity fade only
- Do use `--muted-foreground` for all body copy and secondary text within `.surface-marketing` — it is a solid token with verified WCAG 2.2 AA contrast (≥ 7:1) across canvas, card, and raised-card surfaces. Never replace it with a hardcoded opacity value for informational text
- Do not use raw white-opacity values for any text that conveys information in `.surface-marketing`; if a decorative label absolutely requires opacity, the minimum is 60% white — below that, WCAG AA cannot be guaranteed on the raised card surface (`#1E1E28`). The 30% and 45% levels fail on raised surfaces (4.4:1 and below) and must never carry text
- Do verify WCAG 2.2 AA contrast (4.5:1 minimum for normal text, 3:1 for large text ≥ 24px/18px bold) for each product theme's `--cairn-brand-400` used as eyebrow text on `mkt-canvas`
- Do fill solid buttons and brand-coloured text with `brand-solid` (brand-700) and never with brand-500 — white on brand-500 fails AA (3.4–4.6:1). Reserve brand-500 for focus rings, 0.5px borders, and large display accents
- Do use `neutral-text` (#6B6560) for secondary and helper text, table headers, ghost labels, and placeholders — `neutral-mid` (#78716C) only reaches 4.4:1 on the stone canvas and is decorative/icon-only
- Don't fill a destructive button with the soft Ember (#E05B40) and white text (3.7:1) — use `error-solid` (#A8341C) for filled, or `error-text` on `error-muted` for the subtle variant
- Do check each new product's `--cairn-brand-700` against white (≥4.5:1) when authoring a theme, since it is now the solid-button fill
- Don't mix radius scales within the same view — `rounded.md` on buttons and `rounded.lg` on cards is correct; `rounded.lg` on buttons is not
- Do use `mono` typography for all financial figures in data tables requiring column alignment
- Don't give "Sign in" a button border in the marketing nav — it must remain a plain text link so it does not compete with the primary CTA
- Do use Phosphor as the single icon library across all products and surfaces — never mix it with another icon set
- Do default to Phosphor Regular, stepping up to Bold only at ≤16px and on the dark sidebar, and to Fill only for active/selected states — blanket-bolding icons reads as heavy as over-using 600
- Do use `neutral-mid` (#78716C) for decorative app icons and `ink`/`brand-solid` only for genuinely interactive ones — brand colour on a non-interactive icon breaks the brand-equals-interactive rule
- Do use Phosphor Duotone with a brand foreground (`primary-light`) for marketing feature-card glyphs and app empty/onboarding states — it tints the 20% back layer automatically and reads as a light source on the dark canvas
- Don't use Duotone in dense working app UI at 16–20px — the back layer muddies at small sizes and competes with the interactivity signal
- Do give any icon-only control an accessible name (`aria-label`) and verify icons clear 3:1 against their background as non-text UI elements
