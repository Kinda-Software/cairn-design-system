---
version: alpha
name: Cairn
description: Named after the stone trail markers of the Peak District — Cairn guides designers and agents through consistent, purposeful UI decisions. Supports two distinct surface types (App UI and Marketing UI) across multiple products sharing a common foundation with per-product brand colour theming.
colors:
  # ════════════════════════════════════════════════════════════════
  # THREE-LAYER TOKEN ARCHITECTURE
  #   Layer 1 — global palette ramps (raw values, never used directly)
  #   Layer 2 — semantic tokens per palette (light values shown; dark noted)
  #   Layer 3 — component tokens (see the `components:` block below)
  # Hexes below are the DEFAULT product (Orbit). data-theme re-authors the
  # Layer 1 ramps per product; Layers 2 & 3 re-derive automatically.
  # ════════════════════════════════════════════════════════════════

  # ── LAYER 1 · Primary ramp (Orbit indigo) ──
  primary-50: "#EFF5FF"
  primary-100: "#DFEAFF"
  primary-200: "#C3D5FF"
  primary-300: "#A2B9FF"
  primary-400: "#8198FF"        # dark-mode solid stop
  primary-500: "#667BEF"        # vibrant accent / focus ring — fails AA as white-text bg
  primary-600: "#5263D4"
  primary-700: "#404DB3"        # light-mode solid stop — ≥6.2:1 with white
  primary-800: "#303A8D"
  primary-900: "#212A65"        # nav background
  primary-950: "#13193F"        # deep nav
  # ── LAYER 1 · Secondary ramp (Orbit teal) ──
  secondary-50: "#E9F9F9"
  secondary-100: "#D3F3F2"
  secondary-200: "#AAE5E4"
  secondary-300: "#76D2D1"
  secondary-400: "#3EB6B6"
  secondary-500: "#009B9C"
  secondary-600: "#008485"
  secondary-700: "#006B6C"      # light-mode solid stop
  secondary-800: "#005354"
  secondary-900: "#003B3C"
  secondary-950: "#002424"
  # ── LAYER 1 · Accent ramp (Orbit amber) ──
  accent-50: "#FFF3E5"
  accent-100: "#FFE7CB"
  accent-200: "#FCCF9D"
  accent-300: "#F1B164"
  accent-400: "#DA9026"
  accent-500: "#BF7300"
  accent-600: "#A65D00"
  accent-700: "#8A4800"         # light-mode solid stop
  accent-800: "#6C3600"
  accent-900: "#4D2600"
  accent-950: "#2F1600"
  # ── LAYER 1 · Neutral ramp (shared warm stone — never pure grey) ──
  neutral-50: "#F6F5F4"         # app canvas
  neutral-100: "#EDEBE8"
  neutral-200: "#DBD7D3"        # borders
  neutral-300: "#C4BFB9"
  neutral-400: "#A7A19A"        # dark-mode secondary text
  neutral-500: "#8D867F"        # decorative/icon stop only
  neutral-600: "#767069"
  neutral-700: "#5F5A54"        # secondary TEXT stop — clears 4.5:1 on canvas
  neutral-800: "#494540"
  neutral-900: "#34312D"        # dark-mode card
  neutral-950: "#1F1D1B"        # dark-mode canvas
  # ── LAYER 1 · Base + status + marketing primitives ──
  white: "#FFFFFF"
  ink: "#18181A"                # primary text / dark-mode contrast
  sage: "#16A269"               # success icon/border
  sage-muted: "#D1FAE5"
  sage-text: "#065F46"          # success solid/text
  ember: "#E05B40"              # soft/icon ember — fails white text, never a solid-button fill
  ember-solid: "#A8341C"        # solid destructive fill — 6.6:1 with white
  ember-muted: "#FEF0ED"
  ember-text: "#991B1B"
  error-badge: "#FEE2E2"
  warning-muted-raw: "#FEF3C7"
  warning-text-raw: "#92400E"
  mkt-canvas: "#0D0D12"
  mkt-surface: "#16161E"
  mkt-surface-raised: "#1E1E28"

  # ── LAYER 2 · Semantic tokens (recipe: bg 50·subtle 100·muted 200·
  #    emphasized 300·solid 700·fg 700·contrast white. DARK inverts:
  #    bg 950·subtle 900·muted 800·emphasized 700·solid 400·fg 300·contrast ink) ──
  primary-bg: "#EFF5FF"
  primary-subtle: "#DFEAFF"
  primary-muted: "#C3D5FF"
  primary-emphasized: "#A2B9FF"
  primary-solid: "#404DB3"      # = primary-700 (light) / primary-400 (dark). White-text fill, AA-safe.
  primary-fg: "#404DB3"         # palette-tinted text on a neutral surface
  primary-contrast: "#FFFFFF"   # text/icon on primary-solid (ink in dark mode)
  secondary-bg: "#E9F9F9"
  secondary-subtle: "#D3F3F2"
  secondary-muted: "#AAE5E4"
  secondary-emphasized: "#76D2D1"
  secondary-solid: "#006B6C"
  secondary-fg: "#006B6C"
  secondary-contrast: "#FFFFFF"
  accent-bg: "#FFF3E5"
  accent-subtle: "#FFE7CB"
  accent-muted: "#FCCF9D"
  accent-emphasized: "#F1B164"
  accent-solid: "#8A4800"
  accent-fg: "#8A4800"
  accent-contrast: "#FFFFFF"
  neutral-bg: "#F6F5F4"
  neutral-subtle: "#EDEBE8"
  neutral-muted: "#DBD7D3"
  neutral-emphasized: "#C4BFB9"
  neutral-solid: "#5F5A54"
  neutral-fg: "#5F5A54"
  neutral-contrast: "#FFFFFF"
  # Surface semantics (palette-independent). DARK: background #18181A,
  # card #232325, foreground #F6F5F4, muted-foreground #A7A19A, border #3A3A3C.
  background: "#F6F5F4"
  foreground: "#18181A"
  card: "#FFFFFF"
  card-foreground: "#18181A"
  border: "#DBD7D3"
  muted-foreground: "#5F5A54"   # secondary/helper text — AA on canvas and white card
  focus-ring: "#667BEF"         # primary-500 (non-text UI element, ≥3:1)
  # Status semantics
  success-solid: "#065F46"
  success-muted: "#D1FAE5"
  success-fg: "#065F46"
  error-solid: "#A8341C"        # filled destructive (white label, 6.6:1)
  error-muted: "#FEF0ED"
  error-fg: "#991B1B"           # subtle destructive label + text on error-muted
  warning-muted: "#FEF3C7"
  warning-fg: "#92400E"
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
    decorative: "{colors.neutral-500}"       # icon/decorative stop, never informational
    interactive: "{colors.ink}"              # actionable icon at rest (light content area)
    active: "{colors.primary-solid}"         # selected interactive icon in light content
    sidebar-rest: "rgba(255,255,255,0.65)"   # matches nav-item-rest label
    sidebar-active: "{colors.white}"         # full-opacity white, matches nav-item-active
    status: "Sage (success) / Ember (error) — never the brand colour"
    duotone-foreground: "{colors.primary-400}"  # primary-400 on dark; primary-solid on light
  duotoneSecondaryOpacity: 0.20  # Phosphor duotone back layer — auto-tints from foreground
# ── LAYER 3 · component tokens — each slot binds a Layer 2 semantic token ──
components:
  button-primary:
    backgroundColor: "{colors.primary-solid}"   # 700 stop, not 500 — white label needs ≥4.5:1
    textColor: "{colors.primary-contrast}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-primary-hover:
    backgroundColor: "primary-solid darkened ~6% L (--primary-solid-hover)"
    textColor: "{colors.primary-contrast}"
  button-secondary:
    backgroundColor: "{colors.neutral-subtle}"   # neutral-toned alternative action
    textColor: "{colors.foreground}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-ghost:
    backgroundColor: "transparent"               # hover fills with {colors.primary-bg}
    textColor: "{colors.neutral-fg}"             # neutral-700 — clears AA on the stone fill
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-destructive:                            # subtle/soft destructive
    backgroundColor: "{colors.error-muted}"
    textColor: "{colors.error-fg}"               # ember-text passes (soft ember failed at 3.3:1)
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  button-destructive-solid:                      # filled destructive (white label)
    backgroundColor: "{colors.error-solid}"      # ember-solid, 6.6:1 with white
    textColor: "{colors.white}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 16px
  badge:
    typography: "{typography.caption}"
    rounded: "{rounded.full}"
    padding: 3px 10px
  badge-active:                                  # brand state — uses Primary palette
    backgroundColor: "{colors.primary-muted}"
    textColor: "{colors.primary-fg}"
  badge-secondary:                               # uses Secondary palette
    backgroundColor: "{colors.secondary-muted}"
    textColor: "{colors.secondary-fg}"
  badge-accent:                                  # uses Accent palette
    backgroundColor: "{colors.accent-muted}"
    textColor: "{colors.accent-fg}"
  badge-success:
    backgroundColor: "{colors.success-muted}"
    textColor: "{colors.success-fg}"
  badge-error:
    backgroundColor: "{colors.error-badge}"
    textColor: "{colors.error-fg}"
  badge-warning:
    backgroundColor: "{colors.warning-muted}"
    textColor: "{colors.warning-fg}"
  badge-neutral:
    backgroundColor: "{colors.neutral-muted}"
    textColor: "{colors.neutral-fg}"
  input-default:
    backgroundColor: "{colors.card}"
    textColor: "{colors.foreground}"
    borderColor: "{colors.border}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 36px
    padding: 7px 12px
  input-focus:
    backgroundColor: "{colors.card}"
    textColor: "{colors.foreground}"
    borderColor: "{colors.focus-ring}"           # primary-500; ring at 12% opacity over it
  card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.lg}"
    padding: 16px 20px
  table-header:
    textColor: "{colors.muted-foreground}"       # neutral-700 — passes on canvas and white cards
    typography: "{typography.caption}"
    height: 36px
    padding: 0px 12px
  table-row:
    textColor: "{colors.foreground}"
    typography: "{typography.body-sm}"
    height: 44px
    padding: 0px 12px
  table-row-compact:
    textColor: "{colors.foreground}"
    typography: "{typography.body-sm}"
    height: 32px
    padding: 0px 12px
  table-row-hover:
    backgroundColor: "{colors.neutral-subtle}"
  nav-sidebar:
    backgroundColor: "{colors.primary-950}"
    width: 192px
  nav-item-rest:
    textColor: "rgba(255,255,255,0.65)"
    rounded: "{rounded.md}"
    padding: 6px 8px
  nav-item-active:
    backgroundColor: "rgba(91,110,225,0.15)"     # primary-500 @ 15%
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
    padding: 6px 8px
  nav-item-hover:
    backgroundColor: "rgba(255,255,255,0.06)"
    textColor: "rgba(255,255,255,0.85)"
  mkt-button-primary:
    backgroundColor: "{colors.primary-solid}"    # AA-safe fill; CTA glow shadow supplies luminosity
    textColor: "{colors.primary-contrast}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    height: 40px
    padding: 11px 22px
  mkt-button-primary-large:
    backgroundColor: "{colors.primary-solid}"
    textColor: "{colors.primary-contrast}"
    rounded: "{rounded.md}"
    height: 50px
    padding: 14px 28px
  mkt-button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
    height: 40px
    padding: 11px 22px
  mkt-button-text:
    backgroundColor: "transparent"
    textColor: "{colors.primary-400}"
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

Cairn is a multi-product SaaS design system built around restraint and purpose. It supports two distinct surface types — **App UI** and **Marketing UI** — that share a typographic and structural foundation but follow different rules for how design elements are used.

**Cairn is a set of instructions, not a catalogue.** You don't pick a button from a rack of colours, sizes, and styles. You choose the pattern whose *role* fits the job, and the styling follows. Reach for the Primary button because it's the one action that moves the task forward — not because you fancied a filled indigo control. The fill, the contrast, the height are already decided. Say what an element is *for*, and Cairn tells you what it looks like.

## Component foundation

**shadcn-svelte is the default component set for all Kinda products.** Cairn does not define bespoke components from scratch — it defines the tokens, constraints, and usage guidelines that are applied on top of shadcn-svelte's component library.

This means:

- **shadcn-svelte provides the component implementations** — buttons, inputs, badges, cards, tables, dialogs, and so on. You own the files (shadcn copies them into your repo), so customisation is direct rather than via overrides.
- **Cairn provides a three-layer token system** — global palette ramps (Layer 1) → semantic tokens (Layer 2) → component tokens (Layer 3). shadcn's variable layer (`--background`, `--primary`, `--border`, etc.) is a downstream consumer of Layers 2 and 3, so every shadcn component keeps working while Cairn's warm stone neutrals and brand palettes replace shadcn's defaults.
- **Cairn provides the usage guidelines** — which variants to use in which contexts, what constraints apply (no gradients on buttons, no zebra stripes on tables, one primary action per view), and how components behave differently on the App UI versus Marketing surface.
- **Cairn provides the per-product theming model** — the `data-theme` attribute. Each product re-authors only its Layer 1 ramps; Layers 2 and 3 (and the shadcn bridge) re-derive automatically.

For setup, token mapping, and component-level override code, see [cairn-shadcn.md](./cairn-shadcn.md). The sections below document the intended behaviour and constraints — the *what* and *why*, not the *how*.

**Typeface:** Space Grotesk (400, 500, 600) for all UI and marketing text. Space Mono (400, 700) exclusively for code, numeric financial tables, and technical identifiers. Both fonts share design DNA — the pairing feels intentional rather than assembled.

**Multi-product architecture:** The system hosts multiple products, each with its own brand palettes. All products share the same typography, spacing, radius, and motion; the warm stone Neutral palette is shared by default but a product may author its own (see Per-product theming). Each product authors its own Primary, Secondary and Accent ramps (50→950); the default product is Orbit (indigo Primary, teal Secondary, amber Accent). Products are themed via a `data-theme` attribute on the root element, which re-authors the Layer 1 ramps. The semantic (Layer 2) and component (Layer 3) tokens reference those ramps, so they update automatically.

**App UI surface:** Task-based and information-dense. The job is to help people get their work done. Brand colour appears only on interactive elements. Warm-tinted stone neutrals carry all surface structure. Personality lives in the font details, nowhere else.

**Marketing surface:** Persuasion-based. The job is to build confidence, show the value, and drive conversion. A dark canvas (`mkt-canvas`, #0D0D12) is the default — it makes the brand colour read as a light source rather than a tint, which gives the page more energy. Marketing tokens use the `mkt-` prefix and are additive — they never override app tokens.

## Colours

Cairn organises colour as a **three-layer token system**. Components only ever reference Layer 2 or Layer 3 — they are unaware of which product is active or which mode is set. Swap a Layer 1 ramp behind the tokens and every component updates automatically. Cairn uses warm-tinted stone neutrals rather than pure grey — the slight warmth prevents surfaces from feeling clinical. Brand colour is strictly functional: it signals interactivity in the app and acts as a light source in marketing. Two status families remain reserved for system state: Sage (success) and Ember (error/destructive).

### Layer 1 — global palettes

Four palettes — **Primary**, **Secondary**, **Accent**, **Neutral** — each a full ramp of eleven stops: `50, 100, 200, 300, 400, 500, 600, 700, 800, 900, 950`. These are raw values (`--cairn-primary-500`, `--cairn-neutral-200`, …) and are **never referenced directly** by components. The default product (Orbit) ships indigo Primary, teal Secondary, amber Accent; Neutral is shared warm stone across all products. Per-product themes re-author Primary/Secondary/Accent only.

The `500` stop is the vibrant accent of each ramp (focus rings, 0.5px borders, large display accents) — it is **not** AA-safe behind white text (≈3.4–4.6:1), so it never fills a button or carries normal-size text. The `700` stop is the light-mode solid fill (≥6.2:1 with white); the `400` stop is the dark-mode solid fill (≥6.4:1 with ink).

### Layer 2 — semantic tokens

Every palette exposes the same seven-slot recipe, so components treat all four palettes identically. Each slot is defined for **both light and dark mode**:

| Token | Role | Light | Dark |
|---|---|---|---|
| `{palette}-bg` | lightest wash / page-level palette surface | `50` | `950` |
| `{palette}-subtle` | hover on ghost items, selected rows | `100` | `900` |
| `{palette}-muted` | badge / chip fills | `200` | `800` |
| `{palette}-emphasized` | stronger fills, active fills, palette borders | `300` | `700` |
| `{palette}-solid` | bold fill behind contrast text — AA-safe | `700` | `400` |
| `{palette}-fg` | palette-tinted text on a neutral surface | `700` | `300` |
| `{palette}-contrast` | text/icon colour that sits on `-solid` | white | ink |

`{palette}-solid-hover` darkens (light) or lightens (dark) the solid fill by ~6% lightness, hue-locked. Alongside the palette slots, Layer 2 defines palette-independent **surface semantics** (`background`, `foreground`, `card`, `border`, `muted-foreground`, `focus-ring`) and **status semantics** (`success-solid/-muted/-fg`, `error-solid/-muted/-fg`, `warning-muted/-fg`). `muted-foreground` (neutral-700) is the secondary/tertiary text stop — captions, table headers, ghost labels, placeholders, helper text — clearing 4.5:1 on both the stone canvas and white cards. The decorative neutral-500 stop is reserved for icons and ornament, never informational text.

- **Error semantics:** the soft Ember (`ember`, #E05B40) is for icons and borders; it fails white-text contrast, so the **subtle** destructive button pairs `error-fg` on `error-muted` and the **filled** destructive button uses `error-solid` (#A8341C, 6.6:1 with white).
- **Marketing Canvas (#0D0D12) / Surface (#16161E):** dark marketing surfaces. Always hardcoded — never inherited from the app theme.

### Layer 3 — component tokens

Element-level slots that bind a Layer 2 semantic token onto a specific component part — e.g. `primaryButtonBackground: {primary-solid}`, `badge-accent.backgroundColor: {accent-muted}`, `nav-sidebar.backgroundColor: {primary-950}`. The full set is in the `components:` block of the frontmatter. The **shadcn variable layer is a downstream consumer of this layer** (`--primary` → `--primary-button-background` → `primary-solid`), so shadcn-svelte components keep working unchanged. shadcn's own `--secondary`/`--accent` carry pre-existing UI meaning (neutral secondary button, ghost-hover tint) and are bridged to the Neutral/Primary palettes; reach the Secondary and Accent brand palettes through the Layer 2/3 tokens directly.

**Per-product theming — pick colours, drop them in, ship.** No bikeshedding: a product theme is two steps, and you never hand-author semantic or component tokens.

- **Step 1 — Pick colours, generate palettes.** Choose your brand colours and generate the 50→950 ramps. **Distil** is the supported generator — it emits Primary, Secondary, Accent **and** Neutral as 11-stop palettes in your choice of CSS variables, Tailwind config, or W3C design-tokens JSON. Take the CSS-variables output and paste it into a `[data-theme]` block, named to Cairn's `--cairn-{palette}-{stop}` convention. That's the whole authoring step.
- **Step 2 — Check/adjust semantic tokens.** Layer 2's default mappings apply automatically — the seven-slot recipe reads fixed stops from each ramp (`solid`←700/400, `muted`←200, `bg`←50, nav←950) in both modes, so every semantic and component slot resolves the moment the ramps land. Spot-check the result and tweak a mapping only if a brand needs it. The two AA guardrails — the `700` stop ≥4.5:1 on white (light solid fill) and the `400` stop ≥4.5:1 on ink (dark solid fill) — are inherent to the recipe and satisfied by construction when the ramp keeps an even 50→950 lightness rhythm; verify, don't hand-tune.

**Neutral is replaceable, not fixed.** Warm stone is the *recommended default* — sharing it across products gives the whole family a common surface character — but it is a normal Layer 1 ramp like the others. To give a product its own neutral, paste Distil's Neutral ramp into its `[data-theme]` block and every surface (`background`, `card`, `border`, `muted-foreground`) retints automatically. Two things to keep right: (1) the `ink`/`white` text-and-contrast primitives are independent of the ramp, so the new neutral's `50`/`100` stops must stay light enough for ink body text to clear AA; (2) the dark-mode `card`, `border`, and `input` surfaces are currently authored as fixed values rather than neutral stops, so a fully custom *dark* neutral means overriding those three as well.

## Typography

Space Grotesk is used across both surfaces. Its double-storey `a`, spurred `G`, curved-tail `t`, and strong numerals give it personality at display sizes while remaining legible at 12px in dense UIs. Space Mono is paired for code and financial figures — both fonts share design DNA, making the pairing feel designed rather than assembled.

**Scale construction:** Both surfaces are built as modular scales from an explicit body anchor. The **app scale is anchored at 14px** with a ratio of ≈1.2 (minor third) — dense and efficient. The **marketing scale is anchored at 16px** with a ratio of ≈1.25 (major third) — more presence and air. Every step is derived from its anchor rather than chosen ad hoc, so the two surfaces stay internally consistent and visibly distinct.

**Weight rule:** 600 is reserved for the largest steps — app `display` (29px) and the marketing `heading`/`display` steps. Space Grotesk 500 is optically heavier than Inter 500, so 500 carries every heading below display and using 600 at smaller sizes produces a heavy, overworked result.

**Tracking rule:** Negative tracking increases with size. App display: −0.03em. Marketing display: −0.04em at 76px (letterforms need maximum compression). Marketing heading: −0.03em at 49px. Body and label tracking is 0; the largest body step (marketing body-lg, 20px) takes a faint −0.005em.

**App scale:** 12px caption → 29px display, anchored at 14px body. Steps: caption 12, body-sm 13, body 14, label 14/500, heading-sm 17, heading-md 20, heading-lg 24, display 29. Tight tracking on headings, neutral on body. Line height 1.6 on body (slightly tighter than default to compensate for Space Grotesk's natural width).

**Marketing scale:** 13px eyebrow → 76px hero, anchored at 16px body. Steps: eyebrow 13, caption 14, body 16, body-lg 20 (lead paragraph), subheading 25, heading 49, display 76. Eyebrows use uppercase with wide positive tracking (+0.09em) in `primary-400` colour — never white, which would compete with the headline for first read. The scale is deliberately larger than the app UI — marketing pages reward confidence.

**Animation rule:** Marketing headlines at the heading step (49px) and above use fade-only animation transitions. Never use translateY on large text — moving text at that scale looks like a rendering error.

## Iconography

**Library:** [Phosphor Icons](https://phosphoricons.com) — MIT licensed, free for commercial use, ~1,250 icons. Phosphor is chosen for two reasons. It is built on a strict geometric grid of circular and square base forms, which echoes Space Grotesk's geometric-grotesque construction without competing with it. And it ships six weights (Thin, Light, Regular, Bold, Fill, Duotone) from a single family, so icon weight can be tuned per surface rather than locked to one stroke — the same flexibility Cairn relies on to hold up across a light content area and the always-dark sidebar. Use one library only; never mix Phosphor with another icon set, as differing grids and stroke logic read as inconsistency even when individual icons are clean.

**Weight rule (mirrors the type weight rule):** Regular is the default everywhere. Step up deliberately, not decoratively. Use **Bold** at small sizes (≤16px) and on the dark sidebar, where a regular-weight line can read thin against #0F1330 — this is the answer to "bold enough for both modes." Reserve **Fill** for active and selected states only, where it pairs with `nav-item-active` to signal the current location. Just as 600 is reserved for the largest type steps, Bold and Fill are reserved for specific roles — blanket-bolding every icon produces the same heavy, overworked result as over-using 600.

**Sizing:** Icons follow the 4px grid. 20px is the default UI size (buttons, toolbar actions, table action menus, nav items). 16px is for inline use within body or caption text and dense tables. 24px is for the app top bar and section headers. An icon paired with text aligns to the text's optical centre, not its baseline. Don't scale a single icon to an off-grid size to fill space — pick the next grid step or adjust the container.

**Colour in the app:** Decorative and informational-support icons use `neutral-500` (#8D867F) — this is the decorative/icon stop and must never carry meaning that text doesn't also carry. Genuinely interactive icons (clickable, tappable) take `ink` at rest and may use `primary-solid` when active or selected — this respects the core app rule that **brand colour signals interactivity and nothing else**. Status icons use the Sage and Ember families per state, never the brand colour. In the dark sidebar, icons inherit the nav item's treatment: 65%-white at rest, full-opacity white when active. As non-text UI elements, icons must clear 3:1 against their background; any icon that is the only label for a control needs an accessible name (`aria-label`).

**Duotone and the brand colour:** Duotone is Phosphor's two-layer weight — a full-strength foreground path plus a back layer at 20% opacity that tints automatically from the foreground colour. Set the foreground to a brand stop and the icon reads as a single brand-coloured glyph with a soft tonal fill, no second colour to manage. This is purpose-built for the **marketing feature cards**, whose 32px containers already specify a brand-tinted background and low-opacity brand border: a duotone glyph in `primary-400` (#8198FF) sits inside that container and glows as a light source on the dark canvas, exactly the effect the marketing surface is reaching for. Duotone is also welcome at larger sizes in **app empty states and onboarding** — moments where a single symbolic icon is the focal point and a brand tint reinforces the conversion-to-app handoff thread. Two constraints: do not scatter duotone through dense, working app UI — at 16–20px the back layer muddies and it fights the brand-equals-interactive rule; and when duotone carries the brand colour on a marketing surface, verify the foreground stop clears 3:1 against the card background as a non-text element (`primary-400` on `mkt-surface` passes; a darker brand stop may not).

## Layout

The layout uses a 4px base spacing unit. All spacing values are multiples of 4. Page gutters: 24px mobile / 40px desktop for app surfaces. Marketing sections use 80px vertical padding desktop / 48px mobile, with generous breathing room and one idea per section.

**App layout model:** Fixed sidebar (192px) plus fluid content area. Top navs are not used in the app — they force all products to share horizontal space and overflow as features grow. The sidebar scales vertically without compression and creates clear spatial separation between navigation (left, always dark) and content (right, mode-dependent).

**Marketing layout model:** Centred max-width content with full-bleed dark section backgrounds. Three reusable section patterns: (1) Hero — centred, full-width, eyebrow → headline → body → CTA pair. (2) Feature split — text one side, UI mockup the other, alternating. (3) Social proof — logo bar plus stat trio with section dividers.

**App top bar:** 44px height, white background in light mode, `neutral-border` bottom border. Shows page title left, page-level actions right. Does not repeat sidebar navigation.

## Elevation & depth

Elevation is expressed through border weight and background contrast — never box shadows in the app UI.

- **Default border:** `0.5px solid neutral-border` — all cards, inputs, table rows
- **Emphasis border:** `0.5px solid` (slightly stronger) — hover states, focus context
- **Featured item:** `1px solid primary` — the only exception to the 0.5px rule. Used for featured pricing cards and comparison highlights. 1px has enough optical weight to differentiate from siblings at card scale without filling the background.
- **App shadows:** Never used
- **Marketing CTA glow:** `box-shadow: 0 0 24px rgba(91,110,225,0.25)` permitted on primary CTA buttons on the dark canvas only — functions as an interactivity signal, not decoration

**Dark mode surface hierarchy inverts:** Light mode — page is lighter (stone-50), cards are lightest (white). Dark mode — page is darkest (ink-950), cards are lighter (ink-900). Same hierarchy logic, opposite direction.

## Shapes

Each radius value maps to a specific element category. Don't mix radius scales within the same view.

- **sm (4px):** Chips, inline tags, checkbox corners, small interactive elements
- **md (8px):** Inputs, buttons, select controls, table action menus
- **lg (12px):** Cards, feature panels, sidebar nav items, modal outer containers
- **xl (16px):** Modal inner containers, sheets, large overlays
- **full (9999px):** Badges, pills, avatars, toggle switches, "most popular" pricing label

No rounded corners on single-sided borders — if using a left or top accent border, `border-radius: 0` applies. Rounded corners only work with full borders on all sides.

## Components

The following guidelines apply to the shadcn-svelte components used in all Kinda products. Each entry describes the Cairn constraints and usage rules — the shadcn component files handle the implementation, and `app.css` handles the token values. Where a component needs class additions or variant changes beyond the default token mapping, those are documented in [cairn-shadcn.md](./cairn-shadcn.md).

Read each entry as a decision, not a menu. Match the job to a role; the styling's already settled. The columns lead with *when to choose* — the look is the consequence.

**Buttons — choose by role, the style follows.** Pick the button whose job matches the action. You never choose a fill colour; each role's styling is settled, and already AA-safe.

| Name | Choose it when… | Style (the consequence) |
|---|---|---|
| **Primary** | this is the one action that initiates or advances the main task in the view — one per view | Solid `primary-solid` (700 stop) fill, `primary-contrast` label. No tints, no gradients. |
| **Secondary** | an alternative or parallel action sits alongside the primary without competing with it | `neutral-subtle` fill, `foreground` label — neutral-toned, so it reads as the quieter choice. |
| **Tertiary** | the action is low-stakes, a toolbar action, or an escape hatch — Cancel, Back, Close | Ghost: transparent at rest, `neutral-fg` label, fills with `primary-bg` on hover. |
| **Destructive** | the action causes permanent or hard-to-reverse data loss | Subtle by default — `error-fg` on `error-muted`. Solid (`error-solid` + white) only when it is the confirming action of a destructive step. Ember family — never a red tint of the brand colour. |

Why the styling lands where it does: `primary-500` is reserved for the focus ring and is *never* a button fill — white text on it fails AA (3.4–4.6:1), while `primary-solid` (700) clears ≥6.2:1. The Tertiary/ghost label uses `neutral-fg` (700), not the lighter `neutral-500`, which fails on the stone hover fill. The subtle destructive pairs `error-fg` on `error-muted`; the solid uses `error-solid` (#A8341C, 6.6:1 with white) — the soft Ember (#E05B40) is for icons and borders only and fails as a white-text fill. *(The Tertiary role maps to the `button-ghost` component token; the role name describes the job, the token name describes the treatment.)*

In the marketing nav, "Sign in" is always a plain text link, never a button. It is for returning users who know what they want and must not compete visually with the primary conversion CTA.

**Badges:** Pill shape only (`rounded.full`). Colour encodes meaning: `badge-active` uses brand colour, `badge-success` uses Sage, `badge-error` uses Ember, `badge-warning` uses amber tint, `badge-neutral` uses stone. Never use brand colour for neutral or archived states.

**Form inputs:** Height 36px. Focus ring: `box-shadow: 0 0 0 3px` of `focus-ring` at 12% opacity plus `focus-ring` (primary-500) border colour (the ring is a non-text UI element, so the vibrant stop is fine here at ≥3:1). Error state: `error-solid` border plus `error-muted` background, with `error-fg` for any inline message. Labels are always visible above the input — no floating labels.

**Data tables:** No zebra stripes — use hover highlight (`table-row-hover`) only. Alternating row colours fragment attention horizontally. Header cells use uppercase 11px tracking at +0.06em so they recede and the eye lands on data. All numeric columns must be right-aligned with `font-variant-numeric: tabular-nums`. Financial figures use `mono` typography for strict column alignment. Total rows use a slightly heavier border (`1px solid`) and `body-md` 500 weight. Density: `table-row` (44px) default, `table-row-compact` (32px) available.

**App sidebar nav:** Always dark (#0F1330) regardless of light/dark mode. Structure top to bottom: product switcher (product icon + wordmark + chevron — opens product panel) → optional section labels (11px/500/uppercase/50%-white — decorative only, never convey critical navigation state) → nav items → user identity footer. `nav-item-active` uses `rgba(brand, 0.15)` fill, full white label, full opacity icon. Product switcher is the multi-product entry point — clicking reveals a panel listing all accessible products.

**Marketing nav:** `mkt-nav` is transparent at page top. `mkt-nav-scrolled` applies `mkt-canvas` background and a `rgba(255,255,255,0.10)` bottom border on scroll (transition: 200ms ease, position: sticky). Signed-out right side: "Sign in" text link (55%-white) → primary CTA (32px height). Signed-in right side: "Go to app →" in `primary-400` + thin divider + avatar. "Go to app" uses `primary-400` not white — white would compete with the active nav link and wordmark.

**Marketing feature cards (`mkt-feature-card`):** Small 32×32px icon container with brand-tinted background and low-opacity brand border. Symbolic, not illustrative — scales across products without bespoke artwork. Title uses `body-md` 500 weight in white (`--foreground`). Body copy uses `body-sm` at `--muted-foreground` — a solid, WCAG 2.2 AA-guaranteed cool-neutral token (`oklch(0.7400 0.0040 275)`) that achieves ≥ 7:1 contrast on all three marketing surface levels. Never substitute a raw white-opacity value for body copy: the effective contrast of opacity-based text varies by surface, and values below 60% cannot guarantee AA compliance on the raised card background.

**Marketing pricing cards:** Standard uses `mkt-pricing-card`. Featured uses `mkt-pricing-card-featured` with `1px solid primary` border override. Never fill the featured card with the brand colour — a colour-filled background reads as "selected" not "recommended" and reduces legibility of the feature list. "Most popular" pill (`rounded.full`, `primary` background, white text) is positioned above the card's top edge.

**The marketing-to-app handoff:** When a user converts (clicks "Start free trial"), the dark sidebar appears immediately as the visual anchor — it signals "you are now in the product." First app load shows an onboarding checklist rather than an empty dashboard, preventing the jarring emptiness after a high-energy marketing conversion. The brand colour (`primary`) is the continuous visual thread: it appears in the marketing CTA button, then immediately in the app sidebar icon and the first active checklist item.

## Do's and don'ts

- Do use brand colour only on interactive elements in the app UI — if it is not tappable or clickable, it should not use the brand colour
- Do keep one primary CTA per section or view — multiple primary buttons destroy visual hierarchy
- Don't use zebra stripes on data tables — use `table-row-hover` highlight only
- Do use the `mkt-` token prefix for all marketing-specific values — marketing tokens must never override app semantic tokens
- Don't apply the marketing dark canvas to app UI surfaces — the two surfaces must remain visually and structurally distinct
- Do use 600 font weight only at 22px and above — Space Grotesk 500 is already optically heavy at smaller sizes
- Don't use status colours (success, error) for branding or decoration — they communicate system state only
- Do use stone neutral tokens (warm-tinted) for all app surfaces — never substitute pure grey (#f5f5f5)
- Don't use box shadows in the app UI — elevation is expressed through border weight and background contrast
- Do author each product's `--cairn-primary-950` (deep nav) stop with care when defining a theme — keep the 50→950 lightness rhythm rather than mechanically darkening the brand colour
- Don't animate marketing headlines (48px+) with translateY — use opacity fade only
- Do use `--muted-foreground` for all body copy and secondary text within `.surface-marketing` — it is a solid token with verified WCAG 2.2 AA contrast (≥ 7:1) across canvas, card, and raised-card surfaces. Never replace it with a hardcoded opacity value for informational text
- Do not use raw white-opacity values for any text that conveys information in `.surface-marketing`; if a decorative label absolutely requires opacity, the minimum is 60% white — below that, WCAG AA cannot be guaranteed on the raised card surface (`#1E1E28`). The 30% and 45% levels fail on raised surfaces (4.4:1 and below) and must never carry text
- Do verify WCAG 2.2 AA contrast (4.5:1 minimum for normal text, 3:1 for large text ≥ 24px/18px bold) for each product theme's `--cairn-primary-400` used as eyebrow text on `mkt-canvas`
- Do fill solid buttons and palette-coloured text with the palette `-solid` token (the 700 stop) and never with the 500 stop — white on 500 fails AA (3.4–4.6:1). Reserve the 500 stop for focus rings, 0.5px borders, and large display accents
- Do use `muted-foreground`/`neutral-fg` (neutral-700, #5F5A54) for secondary and helper text, table headers, ghost labels, and placeholders — `neutral-500` (#8D867F) only reaches the decorative threshold and is icon/ornament-only
- Don't fill a destructive button with the soft Ember (#E05B40) and white text (3.7:1) — use `error-solid` (#A8341C) for filled, or `error-fg` on `error-muted` for the subtle variant
- Do check each new product's 700 stop against white (≥4.5:1) and its 400 stop against ink (≥4.5:1) when authoring a theme, since they are the light- and dark-mode solid fills
- Don't mix radius scales within the same view — `rounded.md` on buttons and `rounded.lg` on cards is correct; `rounded.lg` on buttons is not
- Do use `mono` typography for all financial figures in data tables requiring column alignment
- Don't give "Sign in" a button border in the marketing nav — it must remain a plain text link so it does not compete with the primary CTA
- Do use Phosphor as the single icon library across all products and surfaces — never mix it with another icon set
- Do default to Phosphor Regular, stepping up to Bold only at ≤16px and on the dark sidebar, and to Fill only for active/selected states — blanket-bolding icons reads as heavy as over-using 600
- Do use `neutral-500` (#8D867F) for decorative app icons and `ink`/`primary-solid` only for genuinely interactive ones — brand colour on a non-interactive icon breaks the brand-equals-interactive rule
- Do use Phosphor Duotone with a brand foreground (`primary-400`) for marketing feature-card glyphs and app empty/onboarding states — it tints the 20% back layer automatically and reads as a light source on the dark canvas
- Don't use Duotone in dense working app UI at 16–20px — the back layer muddies at small sizes and competes with the interactivity signal
- Do give any icon-only control an accessible name (`aria-label`) and verify icons clear 3:1 against their background as non-text UI elements
