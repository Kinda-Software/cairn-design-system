---
version: alpha
name: Cairn
description: Named after the stone trail markers of the Peak District — Cairn guides designers and agents through consistent, purposeful UI decisions. Supports two distinct surface types (App UI and Marketing UI) across multiple products sharing a common foundation with per-product brand colour theming.
colors:
  primary: "#5B6EE1"
  primary-light: "#818CF8"
  primary-muted: "#E8EAFF"
  primary-text: "#3A4DC8"
  primary-nav: "#1E2660"
  primary-dark-muted: "#1E254A"
  primary-dark-nav: "#0F1330"
  neutral: "#F5F5F4"
  neutral-raised: "#FFFFFF"
  neutral-border: "#E5E5E3"
  neutral-mid: "#78716C"
  neutral-strong: "#1C1917"
  ink: "#18181A"
  success: "#16A269"
  success-muted: "#D1FAE5"
  success-text: "#065F46"
  error: "#E05B40"
  error-muted: "#FEF0ED"
  error-text: "#991B1B"
  error-badge: "#FEE2E2"
  warning-muted: "#FEF3C7"
  warning-text: "#92400E"
  mkt-canvas: "#0D0D12"
  mkt-surface: "#16161E"
  mkt-surface-raised: "#1E1E28"
typography:
  display:
    fontFamily: Space Grotesk
    fontSize: 30px
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.03em
  heading-lg:
    fontFamily: Space Grotesk
    fontSize: 22px
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.022em
  heading-md:
    fontFamily: Space Grotesk
    fontSize: 18px
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: -0.015em
  label:
    fontFamily: Space Grotesk
    fontSize: 15px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: 0em
  body-md:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: 0em
  body-sm:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0em
  caption:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0.01em
  mono:
    fontFamily: Space Mono
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0em
  mkt-display:
    fontFamily: Space Grotesk
    fontSize: 72px
    fontWeight: 600
    lineHeight: 1.0
    letterSpacing: -0.04em
  mkt-heading:
    fontFamily: Space Grotesk
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: -0.03em
  mkt-subheading:
    fontFamily: Space Grotesk
    fontSize: 28px
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.018em
  mkt-body:
    fontFamily: Space Grotesk
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.7
    letterSpacing: 0em
  mkt-eyebrow:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.09em
  mkt-caption:
    fontFamily: Space Grotesk
    fontSize: 15px
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
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral-raised}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-primary-hover:
    backgroundColor: "{colors.primary-text}"
    textColor: "{colors.neutral-raised}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-ghost:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.neutral-mid}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-destructive:
    backgroundColor: "{colors.error-muted}"
    textColor: "{colors.error}"
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
    textColor: "{colors.neutral-mid}"
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
    textColor: "{colors.neutral-mid}"
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
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral-raised}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 40px
    padding: 11px 22px
  mkt-button-primary-large:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral-raised}"
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

- **Primary (#5B6EE1):** Indigo — the default brand colour (Orbit product). Used exclusively on interactive elements in the app: buttons, focus rings, active states. Never decorative.
- **Primary Light (#818CF8):** Lighter indigo stop for dark mode interactive elements and as the marketing eyebrow accent colour. On dark surfaces it reads as a light source.
- **Primary Muted (#E8EAFF):** Light tint for badge backgrounds, focus rings, and selected states. Flips to `primary-dark-muted` (#1E254A) in dark mode.
- **Neutral (#F5F5F4):** Stone 50 — the app page canvas. Warm-tinted to avoid the clinical feel of pure grey.
- **Neutral Raised (#FFFFFF):** Card and surface backgrounds in light mode.
- **Neutral Border (#E5E5E3):** All structural borders in the app UI. Always 0.5px weight.
- **Ink (#18181A):** Primary text colour.
- **Success (#16A269) / Success Muted (#D1FAE5):** Status states only. Never used for branding or decoration.
- **Error (#E05B40) / Error Muted (#FEF0ED):** Destructive actions and error states only.
- **Marketing Canvas (#0D0D12):** The dark surface for all marketing sections. Always hardcoded — never inherited from the app theme.
- **Marketing Surface (#16161E):** Raised feature cards and panels on the dark canvas.

**Per-product theming:** Each product defines 7 brand CSS custom properties: `--brand-500` (primary), `--brand-400` (dark mode variant — lighter), `--brand-50` (muted fill), `--brand-700` (text on muted), `--brand-900` (nav background), `--brand-dark-muted`, `--brand-dark-nav`. Semantic tokens reference these primitives. Not all brand colours work in all positions — `--brand-dark-nav` in particular must be independently authored per product, not mechanically darkened.

## Typography

Space Grotesk is used across both surfaces. Its double-storey `a`, spurred `G`, curved-tail `t`, and strong numerals give it personality at display sizes while remaining legible at 12px in dense UIs. Space Mono is paired for code and financial figures — both fonts share design DNA, making the pairing feel designed rather than assembled.

**Weight rule:** 600 is reserved for headings at 22px and above only. Space Grotesk 500 is optically heavier than Inter 500 — using 600 at smaller sizes produces a heavy, overworked result.

**Tracking rule:** Negative tracking increases with size. App display: −0.03em. Marketing display: −0.04em at 72px (letterforms need maximum compression). Marketing heading: −0.03em at 48px. Body and label tracking is always 0.

**App scale:** 12px captions → 30px display. Tight tracking on headings, neutral on body. Line height 1.65 for body (slightly tighter than default to compensate for Space Grotesk's natural width).

**Marketing scale:** 13px eyebrows → 72px hero. Eyebrows use uppercase with wide positive tracking (+0.09em) in `primary-light` colour — never white, which would compete with the headline for first read. Section headings at 48px, subheadings at 28px, body at 18px. The scale is deliberately larger than the app UI — marketing pages reward confidence.

**Animation rule:** Marketing headlines at 48px+ use fade-only animation transitions. Never use translateY on large text — moving text at that scale looks like a rendering error. This applies to the new mkt-heading size (48px) and above.

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

**Button hierarchy:** One primary button per view. The primary button uses the full brand colour at full weight — no tints or gradients. Secondary for alternative actions alongside primary. Ghost for tertiary and toolbar actions. Destructive uses Ember colour (error token) — never a red variant of the brand colour.

In the marketing nav, "Sign in" is always a plain text link, never a button. It is for returning users who know what they want and must not compete visually with the primary conversion CTA.

**Badges:** Pill shape only (`rounded.full`). Colour encodes meaning: `badge-active` uses brand colour, `badge-success` uses Sage, `badge-error` uses Ember, `badge-warning` uses amber tint, `badge-neutral` uses stone. Never use brand colour for neutral or archived states.

**Form inputs:** Height 36px. Focus ring: `box-shadow: 0 0 0 3px rgba(91,110,225,0.12)` plus `primary` border colour. Error state: `error` border plus `error-muted` background. Labels are always visible above the input — no floating labels.

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
- Don't mix radius scales within the same view — `rounded.md` on buttons and `rounded.lg` on cards is correct; `rounded.lg` on buttons is not
- Do use `mono` typography for all financial figures in data tables requiring column alignment
- Don't give "Sign in" a button border in the marketing nav — it must remain a plain text link so it does not compete with the primary CTA
