# Handoff: ClearFeed Hero Section (Sunset/Pixel-art Landing)

## Overview
Landing page hero for "ClearFeed" — a student-made games/blog site (Austin LTHS). Sunset sky banner, pixel-art card styling, nav bar, headline, hand-written aside note, three game cards, and a featured post link.

## About the Design Files
The bundled HTML is a **design reference built in HTML** — a prototype of the intended look and behavior, not production code. The attached `hero-8b.html` is the FINAL picked option ("8b") extracted from a larger exploration file that contains many earlier rejected iterations (turns 1–8) — ignore anything not in this extract. Recreate this design in your app's existing framework/environment (React, Vue, etc.) using its established component patterns, not by copying the HTML directly. If no framework exists yet, pick the most suitable one for the project.

## Fidelity
**High-fidelity.** Colors, typography, spacing, and layout are final. Recreate pixel-perfectly.

## Screens / Views

### Hero Section
- **Purpose**: Landing page top section — brand nav, headline pitch, and three game promo cards + one blog post promo.
- **Layout**: Fixed reference canvas 1180×700px (scale/adapt for responsive). Absolute-positioned layers over a sunset sky background.
  - Sky strip: full width, 280px tall, tiled pixel-art PNG background (`sky-strip.png`, 8px source tile scaled to 16×280 via `background-size`, `image-rendering: pixelated`).
  - Sun: an 8-bit style sun made of a 64×64 square plus 4 offset box-shadows (cross/plus shape), positioned right:346px top:110px within the sky strip, with two horizontal "glow" bars beneath it (104×8 and 76×6, semi-transparent cream).
  - Two small cloud pixels (18×18 and 10×10 squares) top-left of sky.
  - Nav bar: glassmorphic pill, inset 34px from edges, top:28px, blurred translucent cream background (`backdrop-filter: blur(14px) saturate(1.4)`), logo mark (24×24 pink square + 8×8 dot) + wordmark "ClearFeed" in Caprasimo, 3 nav items + pink "PLAY" pill button.
  - Headline block: left:34px top:188px, width 404px. H1 "Short headline, two lines, no billboard" (last few words in accent pink), sub-paragraph, and a rotated (-1.4deg) glass note card with a small black "tape" strip decoration.
  - Game cards row: left:474px top:200px, 3 cards (198px wide each, gap 20px), each slightly rotated, pixel-bordered, with a 140px-tall tiled sky-strip art placeholder, colored divider bar, title label, two skeleton text bars, and a PLAY pill.
  - Featured post banner: left:474px bottom:52px right:34px, horizontal card — 128px sky-art strip + title/standfirst + "READ" pill, with hover/active press animation (translate + shadow).
  - Decorative dashed circle placeholder for a "BIRD" sprite (160×160, left:140px bottom:72px).
  - Footer credit line "MADE BY STUDENTS · AUSTIN LTHS" bottom-left, pixel font.

## Interactions & Behavior
- Featured post banner: hover → translate(-2px,-2px) + box-shadow 8px 8px 0; active/press → translate(4px,4px), shadow removed. Uses `steps(1)` timing (instant snap, no easing) — 0.08s.
- Nav "PLAY" and card "PLAY" buttons are visual pills; no interaction spec beyond standard button/link states.

## Design Tokens
Colors (turn-6 palette, in use):
- `--k1..--k6`: #6f9fbe, #8aa4c1, #a5a3bd, #c1a1b6, #dba9b6, #efc7ca (dusk gradient ramp)
- `--g6` #fbeadf (page bg), `--c6` #fff8f1 (card bg), `--ink6` #2e2430 (ink text)
- `--ol6` #6b4a60 (outline/border), `--pk6` #d98da3 / `--pk6d` #ac5d7c (pink accent + dark), `--bl6` #5f93b5 / `--bl6d` #3b6f91 (blue accent + dark)
- Sun: #fff1e6

Typography:
- Headings: Caprasimo (400), serif fallback
- Body/UI: Figtree (400/600/700)
- Pixel/label text: Silkscreen (monospace pixel font), used uppercase for labels like "PLAY", "GAME ONE", credit line

Borders/shadows: pixel-style thick 3px solid borders in `--ol6`, hard-edged box-shadow offsets (6px 6px 0, no blur) rather than soft shadows — consistent "pixel-art" language throughout (no border-radius anywhere in this design).

Spacing: outer page margin 34px; nav/card gaps 20-28px; card internal padding 12-16px.

## Assets
- `sky-strip.png` — pixel-art sunset sky gradient strip, tiled horizontally via CSS background-repeat, used both as the hero sky (16×280 scale) and as background art inside game/post cards at different `background-position` offsets and scales (32×560). Source file included in this bundle.
- Fonts loaded from Google Fonts: Caprasimo, Figtree, Silkscreen (see `<link>`/`@import` in the HTML/CSS).

## Files
- `hero-8b.html` — isolated extract of the final hero design (option 8b) with all needed CSS variables/classes inlined in its own `<style>` block.
- `assets/sky-strip.png` — pixel sky background asset.
- `ClearFeed-Design-full.dc.html` — full original exploration file (all turns/options) for reference/context only, not for direct use.
