# Handoff: Grevon Icon Library

## Overview
A 51-icon set for Grevon AI covering product/operations, business & partners, marketing & growth, guest experience, and common UI utilities. Built to match Grevon's brand iconography spec (Phosphor-style line icons).

## About the Design Files
`Grevon Icon Library.dc.html` in this folder is a **design reference** — an HTML prototype showing every icon at a glance, grouped by category, plus two "in context" mockups (sidebar nav, dashboard cards). It is not production code. The `icons/` folder contains the actual deliverable: each icon as a standalone, ready-to-use SVG file.

## Fidelity
**High-fidelity.** Each icon is a finished 24×24 line-icon SVG matching the brand spec exactly (see Design Tokens below). Use the SVGs directly — no restyling should be needed, only recoloring via `stroke` if your codebase needs a different token/currentColor pattern.

## Assets
`icons/` — 51 SVG files, one per icon. See `manifest.json` for the full label → filename mapping. Each file:
- `viewBox="0 0 24 24"`
- `fill="none"`, `stroke="#1C2128"` (Grevon Navy), `stroke-width="1.6"` (or `1"` for a couple of filled corner-dots inside — see individual files)
- `stroke-linecap="round"`, `stroke-linejoin="round"`
- No `<defs>`, no external references — fully self-contained, safe to inline or import as React/Vue components

To recolor for a dark surface or active/teal state, swap the `stroke` attribute (and any `fill="currentColor"` dots) to `#29BCAF` (Grevon Teal) or `#FFFFFF`, or better: strip the `stroke`/`fill` attributes and drive color with `currentColor` + CSS `color`.

### Categories (see manifest.json for exact grouping)
- **Product & operations** (30 icons): check-in & arrivals, guest messaging, channels & booking, automation & workflows, revenue & upsell, analytics & reporting, AI & synaptic intelligence, rooms & housekeeping, payments, security & access, calendar & scheduling, notifications
- **Business & partners** (5): partnership, business, global reach, agreement, scale
- **Marketing & growth** (5): campaign, target, launch, audience, rating
- **Guest experience** (5): loyalty, concierge, amenity, comfort, destination
- **Common utilities** (6): search, add, close, chevron, more, external link

## Design Tokens
- Stroke color (default): `#1C2128` (Grevon Navy)
- Stroke color (active/accent): `#29BCAF` (Grevon Teal)
- Stroke width: `1.6px` at 24×24 (scale proportionally if resizing)
- Corner style: round caps and joins, no fills except a few small solid dots (door knobs, bow-of-key hole, dial center) — these use `fill="currentColor" stroke="none"`
- No gradients, no duotone, no filled icon variants — matches Grevon brand guideline: "2px stroke, rounded caps and joins. No filled icons."

## Files
- `Grevon Icon Library.dc.html` — full visual reference (all 51 icons + in-context mockups)
- `icons/*.svg` — the 51 standalone icon files
- `manifest.json` — label-to-filename index
