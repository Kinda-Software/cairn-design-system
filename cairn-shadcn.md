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

This table shows how each shadcn-svelte CSS variable maps to Cairn's design system tokens, and the reasoning behind each choice.

| shadcn variable | Cairn token | Hex (light) | Reasoning |
|-----------------|-------------|-------------|-----------|
| `--background` | `neutral-50` | `#F5F5F4` | App page canvas. Stone-tinted warm white — never pure grey. |
| `--foreground` | `ink` | `#18181A` | Primary text. Near-black with a faint warm undertone. |
| `--card` | `neutral-raised` | `#FFFFFF` | Cards sit above the canvas — pure white against stone-50 background gives clear hierarchy. |
| `--card-foreground` | `ink` | `#18181A` | Same as body text. |
| `--popover` | `neutral-raised` | `#FFFFFF` | Dropdowns and popovers use the same raised surface as cards. |
| `--popover-foreground` | `ink` | `#18181A` | — |
| `--primary` | `brand-solid` | `#3A4DC8` | Solid interactive fill = brand-700, **not** brand-500. White text on brand-500 fails AA (4.41:1); brand-700 clears 6.8:1. Dark mode shifts to `brand-400` (#818CF8) with ink text. |
| `--primary-foreground` | `brand-contrast` | `#FFFFFF` | Text/icon on `--primary`. White in light mode, ink in dark mode. |
| `--brand-solid` / `--brand-solid-hover` / `--brand-contrast` | semantic | `#3A4DC8` / −6% L / `#FFFFFF` | The AA-safe interactive trio. Use `bg-brand-solid hover:bg-brand-solid-hover text-brand-contrast` for any solid brand fill. Never fill with brand-500. |
| `--secondary` | `neutral-50` | `#F5F5F4` | Secondary button background — stone surface, not white. |
| `--secondary-foreground` | `ink` | `#18181A` | — |
| `--muted` | `neutral-50` | `#F5F5F4` | Ghost elements, disabled areas, placeholder backgrounds. |
| `--muted-foreground` | `neutral-550` | `#6B6560` | Secondary and tertiary text. Stone-550 reads as "subdued" while clearing 4.5:1 on the stone-50 canvas (5.3:1) as well as white cards — stone-500 (#78716C) only reached 4.4:1 on the canvas. |
| `--accent` | `primary-50` | `#E8EAFF` | Hover state for ghost elements, sidebar active items, selected rows. Light brand tint. |
| `--accent-foreground` | `primary-700` | `#3A4DC8` | Text on accent backgrounds — darker brand stop for contrast. |
| `--destructive` | `ember-solid` | `#A8341C` | Filled delete/critical actions. Ember-solid (6.6:1 with white), **not** soft ember (#E05B40, 3.7:1 — fails). Soft ember is for icons/borders and the subtle destructive variant (`error-text` on `error-muted`). |
| `--destructive-foreground` | `white` | `#FFFFFF` | — |
| `--border` | `neutral-200` | `#E5E5E3` | All structural borders. Used at 0.5px throughout (see base styles). |
| `--input` | `neutral-200` | `#E5E5E3` | Input borders at rest. |
| `--ring` | `primary` | `#5B6EE1` | Focus ring colour. Applied at 12% opacity in the focus-visible rule. |
| `--radius` | `radius-lg` | `12px` | Cairn's card radius is the base. shadcn derives sm/md/xl from this. See radius mapping below. |
| `--sidebar` | nav bg | `#0F1330` | Sidebar is always dark in Cairn — product context, not content. |
| `--sidebar-accent` | brand/15% | `rgba(...)` | Active sidebar item background: brand at 15% opacity. |

### Dark mode changes

| Variable | Light | Dark | Reason |
|----------|-------|------|--------|
| `--background` | stone-50 `#F5F5F4` | ink `#18181A` | — |
| `--card` | white `#FFFFFF` | ink-900 `#232325` | Slightly lighter than background — same hierarchy logic, inverted. |
| `--primary` (`brand-solid`) | brand-700 `#3A4DC8` | brand-400 `#818CF8` | Light: dark stop + white text (≥5.8:1). Dark: lighter stop + ink text (5.9:1) — saturated stops are too heavy on dark backgrounds. |
| `--accent` | brand-50 `#E8EAFF` | brand-dark-muted `#1E254A` | Light tint on dark surface reads as a light bleed, not a badge. |
| `--border` | stone-200 `#E5E5E3` | ink-700 `#3A3A3C` | — |
| `--muted-foreground` | stone-550 `#6B6560` | stone-400 `#A09E97` | Light stop darkened to clear AA on the canvas; dark stop lightened for dark-mode contrast (6.6:1). |

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

The default (primary) variant fills with `--primary`, which now resolves to `brand-solid` (brand-700), not brand-500 — this is what keeps the white label AA-compliant. Don't override the fill back to a brand-500 utility. Hover uses `--brand-solid-hover`. Cairn **never uses gradients** on buttons — ensure no `bg-gradient-*` classes appear in your button component.

### Badge

shadcn's badge uses `rounded-full` — correct per Cairn spec. The default variant maps to Cairn's `badge-neutral`. Create additional variants for the Cairn status states:

```ts
// src/lib/components/ui/badge/index.ts
const badgeVariants = cva(
  "inline-flex items-center rounded-full px-2.5 py-0.5 text-xs font-medium ...",
  {
    variants: {
      variant: {
        default:     "bg-accent text-accent-foreground",       // brand / active
        success:     "bg-success-muted text-success-foreground",
        destructive: "bg-destructive/10 text-destructive",
        warning:     "bg-warning-muted text-warning-foreground",
        outline:     "bg-muted text-muted-foreground border",  // neutral / archived
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

The `eyebrow` utility class applies `text-[13px] font-semibold tracking-[0.09em] uppercase` with `color: var(--cairn-brand-400)` — the brand-muted colour, not white. Marketing body copy is 16px (`--text-mkt-body`); use `text-muted-foreground` for secondary copy, never a raw white-opacity value (see Design.md).

---

## Adding a new product theme

1. Define the 7 brand primitive values in `app.css` under a new `[data-theme]` selector
2. Set `data-theme="your-product"` on `<html>` in your layout
3. Check WCAG AA contrast (4.5:1): `--cairn-brand-700` against white (it is the solid-button fill via `brand-solid`), `--cairn-brand-400` against `mkt-canvas` and ink (dark-mode interactive + eyebrow), and `--cairn-brand-700` against `--cairn-brand-50` (accent text)
4. Independently author `--cairn-brand-dark-nav` — do not mechanically darken the brand colour

```css
/* app.css */
[data-theme="newproduct"] {
  --cairn-brand-500:        oklch(...); /* primary interactive */
  --cairn-brand-400:        oklch(...); /* dark mode variant — lighter */
  --cairn-brand-50:         oklch(...); /* light muted fill */
  --cairn-brand-700:        oklch(...); /* text on brand-50 background */
  --cairn-brand-900:        oklch(...); /* nav background (light mode) */
  --cairn-brand-dark-muted: oklch(...); /* dark mode badge fill */
  --cairn-brand-dark-nav:   oklch(...); /* dark mode nav — independently chosen */
}
```
