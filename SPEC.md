# Daily Motivation Dashboard

## Concept & Vision

A serene, zen-like dashboard that greets you with a fresh motivational quote each day. The experience should feel like opening a mindfulness app — calm, centered, and inspiring. The quote is the hero; everything else recedes to support it.

## Design Language

**Aesthetic Direction:** Soft minimalism with warm paper-like textures — inspired by Japanese stationary and morning light through shoji screens.

**Color Palette:**
- Background: `#faf9f7` (warm off-white, like aged paper)
- Primary text: `#2d2a26` (soft charcoal)
- Secondary text: `#8a8580` (muted stone)
- Accent: `#c9a87c` (warm gold, used sparingly)
- Card background: `#ffffff` with subtle shadow

**Typography:**
- Quote text: `Cormorant Garamond` (elegant serif with literary feel) — 400 weight, 2.2rem
- Author: `Inter` — 500 weight, 0.9rem, uppercase tracking
- UI elements: `Inter` — 400 weight

**Spatial System:**
- Generous whitespace; the quote floats in center with ample breathing room
- 8px base unit; spacing in multiples (16, 24, 32, 48, 64)

**Motion Philosophy:**
- Slow, meditative transitions (400-600ms)
- Quote fades in gently on load (opacity + subtle upward drift)
- Refresh action has a calm crossfade
- Subtle floating animation on decorative elements

**Visual Assets:**
- Simple geometric accent (thin gold line or circle)
- No icons; typography and whitespace are the UI

## Layout & Structure

Single-page, vertically centered composition:

```
┌─────────────────────────────────────┐
│                                     │
│           [thin gold line]          │
│                                     │
│      "The only way to do great      │
│       work is to love what you      │
│       do."                          │
│                                     │
│            — Steve Jobs             │
│                                     │
│           [date + refresh]          │
│                                     │
└─────────────────────────────────────┘
```

- Full viewport height, content centered
- Subtle paper texture overlay on background
- Small decorative gold line above quote
- Quote in elegant serif, author in small caps below
- Date displayed subtly; small refresh icon (no fill, just outline)

**Responsive:** Works beautifully from 320px to 4K. Quote text scales fluidly.

## Features & Interactions

**Core Features:**
1. Daily quote rotation — same quote all day, changes daily
2. Manual refresh — clicking refresh shows a new random quote with crossfade
3. Current date display — elegant, unobtrusive

**Interactions:**
- Refresh button: hover scales up 1.05x with 200ms ease; click triggers crossfade animation (current quote fades out while new fades in)
- Subtle entrance animation on page load: quote drifts up from 20px below while fading in over 800ms

**Edge Cases:**
- Quotes stored locally in JS array (20+ curated quotes)
- No network dependency — works offline immediately

## Component Inventory

**Quote Card:**
- No visible border; soft shadow (`0 4px 24px rgba(0,0,0,0.06)`)
- Padding: 48px 64px on desktop, 32px 24px on mobile
- Max-width: 640px

**Decorative Line:**
- Width: 48px, height: 1px, color: `#c9a87c`
- 32px margin below

**Refresh Button:**
- 32x32px hit area
- SVG icon, stroke color `#8a8580`
- Hover: stroke transitions to `#c9a87c`
- Active: scale 0.95

**Date Display:**
- Font-size: 0.75rem
- Color: `#8a8580`
- Letter-spacing: 0.1em

## Technical Approach

- Single HTML file with embedded CSS and JS
- Vanilla JS — no frameworks needed for this scope
- Google Fonts loaded via `<link>` (Cormorant Garamond, Inter)
- Quotes stored as JS array with quote text and author
- `Date` object used to select daily quote (day of year % quotes.length)
- CSS transitions for all animations