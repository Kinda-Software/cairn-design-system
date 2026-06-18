# Cairn × shadcn-svelte Integration

> **This is the technical setup and token-mapping reference.** shadcn-svelte is the default component set for all Kinda products — Cairn provides the CSS tokens, theming model, and usage guidelines that sit on top of it. For usage guidelines and design constraints, see [Design.md](./Design.md).

## Setup

### 1. Install shadcn-svelte with Tailwind v4

```bash
npx shadcn-svelte@latest init
```

When prompted:
- Style: **new-york**
- Base colour: **stone** (closest to Cairn's warm neutrals — will be overridden anyway)
- CSS variables: **yes**

### 2. Replace `app.css`

Delete the generated `src/app.css` and replace it with the Cairn theme file. Then add the Google Fonts import to your `app.html`:

```html
<!-- src/app.html -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
```

### 3. Set the product theme

In your root `+layout.svelte`, set the `data-theme` attribute:

```svelte
<script>
  // The active product — set this from your app config
  const product = 'orbit'; // 'orbit' | 'beacon' | 'vault' | 'pulse'
</script>

<html data-theme={product} lang="en">
  <body>
    <slot />
  </body>
</html>
```

### 4. Dark mode with mode-watcher

```bash
npx shadcn-svelte@latest add mode-watcher
```

```svelte
<!-- src/routes/+layout.svelte -->
<script>
  import { ModeWatcher } from 'mode-watcher';
</script>

<ModeWatcher />
<slot />
```

---

## Token mapping

The shadcn variable layer is a **downstream consumer** of Cairn's Layer 2 (semantic) and Layer 3 (component) tokens. shadcn vars resolve through the component token, which resolves through a Layer 2 semantic token, which resolves through a Layer 1 ramp stop — so a `data-theme` swap or mode flip updates everything automatically. Hexes below are the default Orbit product (light mode).

| shadcn variable | Resolves through | Hex (light) | Reasoning |
|-----------------|------------------|-------------|-----------|
| `--background` | `neutral-50` | `#F6F5F4` | App page canvas. Stone-tinted warm white — never pure grey. |
| `--foreground` | `ink` | `#18181A` | Primary text. Near-black with a faint warm undertone. |
| `--card` | `card` → white | `#FFFFFF` | Cards sit above the canvas — pure white against stone-50 gives clear hierarchy. |
| `--card-foreground` | `ink` | `#18181A` | Same as body text. |
| `--popover` | `card` → white | `#FFFFFF` | Dropdowns and popovers use the same raised surface as cards. |
| `--popover-foreground` | `ink` | `#18181A` | — |
| `--primary` | `--primary-button-background` → `primary-solid` (700) | `#404DB3` | Solid interactive fill = 700 stop, **not** 500. White on 500 fails AA (≈4.4:1); 700 clears 7.2:1. Dark mode shifts to the 400 stop (`#8198FF`) with ink text. |
| `--primary-foreground` | `primary-contrast` | `#FFFFFF` | Text/icon on `--primary`. White in light, ink in dark. |
| `--secondary` | `--secondary-button-background` → `neutral-subtle` | `#EDEBE8` | Secondary button background — neutral-toned alternative action, not white. |
| `--secondary-foreground` | `foreground` | `#18181A` | — |
| `--muted` | `neutral-subtle` | `#EDEBE8` | Ghost elements, disabled areas, placeholder backgrounds. |
| `--muted-foreground` | `neutral-700` | `#5F5A54` | Secondary/tertiary text. Clears 4.5:1 on both the stone canvas and white cards. neutral-500 (#8D867F) is decorative/icon-only. |
| `--accent` | `primary-bg` (50) | `#EFF5FF` | Hover state for ghost elements, sidebar active items, selected rows. Light brand tint. |
| `--accent-foreground` | `primary-fg` (700) | `#404DB3` | Text on accent backgrounds — darker brand stop for contrast. |
| `--destructive` | `--destructive-button-background` → `error-solid` | `#A8341C` | Filled delete/critical actions. Ember-solid (6.6:1 with white), **not** soft ember (#E05B40, 3.7:1 — fails). Soft ember is for icons/borders and the subtle destructive variant (`error-fg` on `error-muted`). |
| `--destructive-foreground` | `white` | `#FFFFFF` | — |
| `--border` | `neutral-200` | `#DBD7D3` | All structural borders. Used at 0.5px throughout (see base styles). |
| `--input` | `input-border` → `neutral-200` | `#DBD7D3` | Input borders at rest. |
| `--ring` | `input-ring` → `focus-ring` (primary-500) | `#667BEF` | Focus ring colour. Applied at 12% opacity in the focus-visible rule. |
| `--radius` | `radius-lg` | `12px` | Cairn's card radius is the base. shadcn derives sm/md/xl from this. See radius mapping below. |
| `--sidebar` | `primary-950` | `#13193F` | Sidebar is always dark in Cairn — product context, not content. |
| `--sidebar-accent` | primary-500 / 15% | `rgba(...)` | Active sidebar item background: primary at 15% opacity. |

> **Secondary & Accent brand palettes:** shadcn's own `--secondary` and `--accent` carry pre-existing UI meaning (neutral secondary button, ghost-hover tint) and are bridged to the Neutral/Primary palettes above. To use Cairn's **Secondary** (teal) and **Accent** (amber) brand palettes, reach the Layer 2/3 tokens directly via the generated Tailwind utilities — e.g. `bg-secondary-solid text-secondary-contrast`, `bg-accent-muted text-accent-fg`, or the component tokens `--badge-secondary-background` / `--badge-accent-background`.

### Dark mode changes

| Variable | Light | Dark | Reason |
|----------|-------|------|--------|
| `--background` | stone-50 `#F6F5F4` | ink `#18181A` | — |
| `--card` | white `#FFFFFF` | `#232325` | Slightly lighter than background — same hierarchy logic, inverted. |
| `--primary` (`primary-solid`) | 700 `#404DB3` | 400 `#8198FF` | Light: dark stop + white text (≥6.2:1). Dark: lighter stop + ink text (≥6.4:1) — saturated stops are too heavy on dark backgrounds. |
| `--accent` | primary-bg `#EFF5FF` | primary-900 `#212A65` | Light tint on dark surface reads as a light bleed, not a badge. |
| `--border` | stone-200 `#DBD7D3` | `#3A3A3C` | — |
| `--muted-foreground` | neutral-700 `#5F5A54` | neutral-400 `#A7A19A` | Light stop darkened to clear AA on the canvas; dark stop lightened for dark-mode contrast (6.6:1). |

---

## Radius mapping

shadcn derives its radius scale from the single `--radius` value. Cairn sets `--radius: 12px` (card radius) and the scale is calculated from there.

| shadcn utility | Calculated value | Cairn token | Use |
|----------------|-----------------|-------------|-----|
| `rounded-sm` | ~4px | `radius-sm` | Chips, tags |
| `rounded-md` | ~8px | `radius-md` | Buttons, inputs |
| `rounded-lg` | 12px | `radius-lg` | Cards, panels |
| `rounded-xl` | ~16px | `radius-xl` | Modals, sheets |
| `rounded-full` | 9999px | `radius-full` | Badges, pills, avatars |

---

## Component overrides

Some shadcn components need minor class additions to match Cairn spec precisely. These are not hacks — they're the normal shadcn customisation pattern (you own the component files).

### Button

shadcn generates buttons with `cursor-pointer`. Cairn uses `cursor-default` for buttons (desktop app convention). Open `src/lib/components/ui/button/index.ts` and adjust the variant definitions:

```ts
// In the buttonVariants cva definition, adjust the base class:
base: "... cursor-default ..."
```

Cairn button height is 36px (app) / 40px (marketing). shadcn defaults to `h-9` (36px) — this matches. No change needed for the app surface.

The default (primary) variant fills with `--primary`, which resolves through `--primary-button-background` to `primary-solid` (the 700 stop), not the 500 stop — this is what keeps the white label AA-compliant. Don't override the fill back to a 500-stop utility. Hover uses `--primary-button-background-hover` (`primary-solid-hover`). Cairn **never uses gradients** on buttons — ensure no `bg-gradient-*` classes appear in your button component.

### Badge

shadcn's badge uses `rounded-full` — correct per Cairn spec. The default variant maps to Cairn's `badge-neutral`. Create additional variants for the Cairn status states:

```ts
// src/lib/components/ui/badge/index.ts
const badgeVariants = cva(
  "inline-flex items-center rounded-full px-2.5 py-0.5 text-xs font-medium ...",
  {
    variants: {
      variant: {
        default:     "bg-primary-muted text-primary-fg",          // brand / active
        secondary:   "bg-secondary-muted text-secondary-fg",      // Secondary palette
        accent:      "bg-accent-muted text-accent-fg",            // Accent palette
        success:     "bg-success-muted text-success-foreground",
        destructive: "bg-error-muted text-error-foreground",
        warning:     "bg-warning-muted text-warning-foreground",
        outline:     "bg-muted text-muted-foreground border",     // neutral / archived
      }
    }
  }
)
```

### Card

shadcn cards use `rounded-lg` and `border` by default — both correct. The border is 0.5px via the base layer override in `app.css`. No changes needed.

### Input

shadcn inputs use `h-9` (36px) — matches Cairn spec. The focus ring is handled by the `:focus-visible` rule in `app.css`. No changes needed.

### Table

shadcn's Table component is unstyled by default — apply Cairn table classes:

```svelte
<!-- No zebra stripes. Hover state via Tailwind group hover. -->
<TableRow class="border-b border-border/50 hover:bg-muted transition-colors">
```

For numeric columns, add `text-right tabular-nums font-mono text-sm` to `<TableCell>`.

Table header cells: add `text-[11px] font-medium uppercase tracking-[0.06em] text-muted-foreground` to `<TableHead>`.

### Separator

shadcn separators default to 1px. Override to match Cairn's 0.5px:

```svelte
<Separator class="h-px bg-border opacity-50" />
```

---

## Marketing surface usage

Wrap marketing sections in the `.surface-marketing` class. shadcn components inside this wrapper will automatically use the dark canvas token overrides:

```svelte
<section class="surface-marketing px-10 py-20">
  <!-- shadcn Card inside marketing context -->
  <Card class="border-white/8">
    <CardHeader>
      <p class="eyebrow">Feature</p>
      <CardTitle class="text-white">Your data, always current</CardTitle>
    </CardHeader>
    <CardContent class="text-muted-foreground">
      Changes appear within seconds.
    </CardContent>
  </Card>

  <!-- Marketing primary button — larger than app button -->
  <Button class="h-[50px] px-7 text-[17px]">
    Start free trial
  </Button>
</section>
```

The `eyebrow` utility class applies `text-[13px] font-semibold tracking-[0.09em] uppercase` with `color: var(--cairn-primary-400)` — the lighter primary stop, not white. Marketing body copy is 16px (`--text-mkt-body`); use `text-muted-foreground` for secondary copy, never a raw white-opacity value (see Design.md).

---

## Adding a new product theme

No bikeshedding — pick colours, drop them in, ship. Two steps:

1. **Generate & paste the palettes.** Generate the 50→950 ramps with **Distil** and export as CSS variables. Distil emits Primary, Secondary, Accent and Neutral as 11 evenly-spaced stops in your choice of CSS variables, Tailwind config, or W3C design-tokens JSON. Paste the CSS-variables output into a new `[data-theme]` selector in `app.css` as `--cairn-{palette}-{stop}`. Layers 2 and 3 (and the shadcn bridge) re-derive automatically — you never author a semantic or component token. Neutral defaults to the shared warm stone; include Distil's Neutral ramp only to give this product its own.
2. **Set `data-theme="your-product"`** on `<html>` in your layout, then verify. The AA guardrails are inherent to the recipe and hold by construction when the ramp is evenly spaced (Distil's is) — confirm, don't hand-tune: the `700` stop ≥4.5:1 on white (light solid fill), the `400` stop ≥4.5:1 on ink (dark solid fill), and `primary-400` ≥4.5:1 on `mkt-canvas` (marketing eyebrow). If you replaced Neutral, also confirm its `50`/`100` stops hold ink body text at AA, and override the dark-mode `--card`/`--border`/`--input` values (these are fixed, not neutral stops). Run `npx @google/design.md lint Design.md` — it should exit 0.

```css
/* app.css — paste Distil's CSS-variable output */
[data-theme="newproduct"] {
  /* Primary — 11 stops */
  --cairn-primary-50:   oklch(...);
  /* … 100 200 300 400 500 600 700 800 900 … */
  --cairn-primary-950:  oklch(...);
  /* Secondary — 11 stops (50→950) */
  --cairn-secondary-50: oklch(...);
  /* … */
  /* Accent — 11 stops (50→950) */
  --cairn-accent-50:    oklch(...);
  /* … */
  /* Neutral — optional; omit to keep shared warm stone */
}
```
