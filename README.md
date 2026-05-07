# Cairn Design System

Named after the stone trail markers of the Peak District — Cairn guides consistent UI decisions across Kinda products without getting in the way.

**Live docs:** [https://kinda-software.github.io/cairn-design-system/](https://kinda-software.github.io/cairn-design-system/)

---

## What's here

| File | Purpose |
|---|---|
| [`index.html`](index.html) | Full documentation site — architecture, tokens, components, setup guides |
| [`Design.md`](Design.md) | Machine-readable design system spec ([google-labs-code/design.md](https://github.com/google-labs-code/design.md) format) |
| [`cairn-shadcn.md`](cairn-shadcn.md) | shadcn-svelte integration guide — setup, token mapping, component overrides |
| [`app.css`](app.css) | Cairn CSS theme file — install into SvelteKit projects to replace the shadcn default palette |

## Quick start

```bash
# 1. Initialise shadcn-svelte in your SvelteKit project
npx shadcn-svelte@latest init
# Style: new-york · Base colour: stone · CSS variables: yes

# 2. Replace src/app.css with the Cairn theme file
# Download: https://kinda-software.github.io/cairn-design-system/app.css

# 3. Set data-theme on your root layout's <html> element
# 'orbit' | 'beacon' | 'vault' | 'pulse'
```

See [`cairn-shadcn.md`](cairn-shadcn.md) for the complete setup walkthrough and [`Design.md`](Design.md) for the full token reference.

## Using with coding agents

`Design.md` follows the [google-labs-code/design.md](https://github.com/google-labs-code/design.md) specification. Point any coding agent at it before generating UI:

```
Read Design.md before generating any UI component for this project.
All colours, typography, spacing, and component behaviour must match
the tokens and constraints defined in that file.
```

Lint the file with the official CLI:

```bash
npx @google/design.md lint Design.md
```

---

Part of [Kinda Software](https://kindasoftware.com) — SaaS tools built for a single goal, as simply as possible.
