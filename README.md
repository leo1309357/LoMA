# LoMA — Retro-Skeuomorphic Visual Design Language

> **Warm surfaces · Tactile controls · Editorial clarity**  
> *Design with the warmth of paper and the precision of an instrument.*

**LoMA** is a lightweight, restrained skeuomorphic visual design language inspired by early Web 2.0 interfaces (circa 2010) and classic editorial print layouts. It restores tactile materiality, crisp hairline boundaries, and directional lighting to modern digital interfaces without sacrificing accessibility, responsiveness, or usability.

---

## Overview

| Property | Details |
| :--- | :--- |
| **Name** | LoMA |
| **Type** | Visual Design Language / UI Theme Specification |
| **Version** | `1.0.0` (Initial Draft) |
| **Date** | 2026-11-26 |
| **Aesthetic** | Restrained Skeuomorphism · Early Web 2.0 · Retro Editorial Typography |
| **Target Platforms** | Websites, content platforms, desktop apps, utility WebUIs, game menus, and codex/wiki interfaces |
| **Reference Blueprint** | `deepseek_html_20261126_c60833.html` (*Pixel Journal*) |

### Visual Signature

Even without hero imagery, LoMA remains immediately recognizable through five core traits:
1. **Warm Paper Canvas** (`#E8E4DC`) with subtle ambient glows and ultra-light diagonal hatching.
2. **Cool Slate-Blue Chrome** (`#4A5A6A` → `#2B3642`) for navigation bars, toolbars, and structural headers.
3. **Molded Amber Controls** (`#E8B04B` → `#C07F1A`) for primary actions and interactive focal points.
4. **Crisp 1px Hairline Borders & Small Radii** (`4px–6px`) paired with consistent top-down lighting.
5. **Editorial Serif Headings** (`Georgia`) paired with clean sans-serif UI/body typography.

---

## Core Design Principles

- **Material Honesty:** Backgrounds feel like paper, content containers like cardstock, navigation bars like dark coated metal, and buttons like molded enamel controls. Materiality shifts strictly according to functional role.
- **Tactile Affordance:** Pressable controls feature subtle elevation, top inner highlights, and bottom shadows—depressing inward on activation. Static surfaces never masquerade as buttons.
- **Editorial Order:** Clear column grids, hairline dividers, and compact yet breathable type hierarchies evoke a well-typeset print magazine.
- **Restrained Ornament:** Textures stay low-contrast and shadows remain short and soft so surface treatments never overpower content.
- **Modern Usability:** Retro aesthetics never excuse archaic UX. Full keyboard navigation, WCAG-compliant contrast ratios, touch-friendly hit targets (`44×44px`), and reduced-motion support are mandatory.

### What LoMA Is Not
- **Not Pure Flat Design:** Key controls retain physical borders, subtle gradients, and press states.
- **Not Heavy Skeuomorphism:** Avoids leather, woodgrain, rivets, gauges, or heavy photographic textures.
- **Not Glassmorphism / Neumorphism:** No backdrop blurs, neon glows, or borderless low-contrast extrusions.
- **Not a Nostalgia Filter:** No CRT scanlines, artificial stains, distortion, or low-res artifacts.

---

## Color System

LoMA defaults to a warm light palette targeting a visual balance of **70–85% warm neutrals**, **10–20% slate-blue chrome**, and **3–10% accent colors**.

### Base Tokens

| Token | Hex | Role |
| :--- | :--- | :--- |
| `--loma-canvas` | `#E8E4DC` | Global warm paper background |
| `--loma-canvas-deep` | `#DDD8CE` | Footer & secondary canvas zones |
| `--loma-surface` | `#FDFCF9` | Cards, body containers, dialogs |
| `--loma-surface-muted` | `#F0ECE3` | Tag pills, secondary panels |
| `--loma-border` | `#D6D0C4` | Structural warm-gray borders |
| `--loma-divider` | `#E3DDD1` | Hairline content dividers |
| `--loma-divider-dashed` | `#DDD6C8` | Dashed list separators |
| `--loma-slate-light` | `#4A5A6A` | Dark chrome top highlight |
| `--loma-slate-mid` | `#35424F` | Dark chrome midtone |
| `--loma-slate-dark` | `#2B3642` | Dark chrome base & heading text |
| `--loma-slate-border` | `#1E262E` | Dark chrome outer border |
| `--loma-amber-light` | `#E8B04B` | Primary button highlight |
| `--loma-amber-mid` | `#D4942A` | Primary button midtone |
| `--loma-amber-dark` | `#C07F1A` | Primary button shadow |
| `--loma-amber-border` | `#A86A10` | Primary button border |
| `--loma-brick` | `#C0392B` | Inline links & text accents |
| `--loma-brick-strong` | `#A2382C` | High-contrast links on paper canvas |
| `--loma-text` | `#3A3A3A` | Default body copy |
| `--loma-text-body` | `#4A4A4A` | Card body copy |
| `--loma-text-muted` | `#736B60` | Metadata on light surfaces |
| `--loma-text-on-canvas-muted` | `#625A4E` | Small text on canvas/footers |
| `--loma-text-amber` | `#2C1B08` | High-contrast text on amber buttons |
| `--loma-text-inverse` | `#F5F2EA` | Text on dark chrome |
| `--loma-text-nav` | `#D8DDE3` | Navigation links |
| `--loma-tag-text` | `#5A6A7A` | Tag label text |
| `--loma-focus` | `#28628A` | Keyboard focus ring |

### Functional Status Colors

| State | Foreground | Background | Presentation |
| :--- | :--- | :--- | :--- |
| **Success** | `#35664E` | `#E8F0E6` | Checkmark icon + status label |
| **Info** | `#345E80` | `#E7EDF3` | Info icon + message |
| **Warning** | `#79500D` | `#F5EAD2` | Warning icon + remediation tip |
| **Error** | `#A2382C` | `#F6E5DF` | Error icon + specific cause |

---

## Materiality, Lighting & Elevation

- **Light Source:** Fixed directly overhead and slightly to the left. Raised controls have lighter tops, 1px top inner highlights, and downward drop shadows; recessed inputs have top inner shadows and zero outer drop shadow.
- **Border Radii:** `4px` for inputs/small controls, `5px` for buttons, `6px` for cards/hero banners/dialogs, and `12px` (pill) strictly for tags/badges.

### Elevation & Shadow Scale

| Level | Token / Value | Usage |
| :--- | :--- | :--- |
| **E0 · Base** | `none` | Paper canvas, text, dividers |
| **E1 · Cardstock** | `0 1px 3px rgb(0 0 0 / 8%), 0 4px 12px rgb(0 0 0 / 5%)` | Content cards, static panels |
| **E2 · Control** | `inset 0 1px 0 rgb(255 255 255 / 40%), 0 1px 2px rgb(0 0 0 / 20%)` | Buttons, raised controls |
| **E3 · Chrome** | `inset 0 1px 0 rgb(255 255 255 / 15%), 0 2px 4px rgb(0 0 0 / 20%)` | Top bars, fixed toolbars |
| **E4 · Overlay** | `0 1px 2px rgb(0 0 0 / 15%), 0 6px 18px rgb(0 0 0 / 12%)` | Hero banners, dropdowns, modals |
| **I1 · Inset** | `inset 0 1px 3px rgb(0 0 0 / 12%)` | Text inputs, progress tracks |
| **I2 · Pressed** | `inset 0 2px 4px rgb(0 0 0 / 25%)` | Active/pressed button state |

---

## Typography & Layout

### Font Stacks
- **Headings / Brand:** `Georgia, "Times New Roman", "Songti SC", "Noto Serif CJK SC", SimSun, serif`
- **UI / Body:** `"Helvetica Neue", Helvetica, Arial, "PingFang SC", "Microsoft YaHei", "Noto Sans CJK SC", sans-serif`
- **Monospace:** `"SFMono-Regular", Consolas, "Liberation Mono", monospace`

### Grid & Responsive Behavior
- **Desktop (`> 760px`):** Centered `960px` max-width container (`20px` horizontal padding) with a fluid main column (`616px`), `24px` gutter, and fixed `280px` sidebar.
- **Mobile (`≤ 760px`):** Collapses into a single-column stack with the sidebar moving beneath main content, card padding tightening from `22px 24px` to `16px`, and navigation collapsing into an accessible expandable menu.
- **Touch & Motion:** Minimum `44×44px` hit areas on coarse pointers (`@media (pointer: coarse)`), `150–200ms` transitions limited to color/shadow/opacity, and full support for `prefers-reduced-motion`.

---

## Quick Start (CSS Implementation)

Drop the core tokens and base component styles into your stylesheet as a starting point, or map the same semantic tokens to non-web engines (e.g., Godot `Theme` / `StyleBox` resources or desktop UI toolkits):

```css
:root {
  /* Paper & surfaces */
  --loma-canvas: #e8e4dc;
  --loma-canvas-deep: #ddd8ce;
  --loma-surface: #fdfcf9;
  --loma-surface-muted: #f0ece3;
  --loma-border: #d6d0c4;
  --loma-divider: #e3ddd1;
  --loma-divider-dashed: #ddd6c8;

  /* Frame */
  --loma-slate-light: #4a5a6a;
  --loma-slate-mid: #35424f;
  --loma-slate-dark: #2b3642;
  --loma-slate-border: #1e262e;

  /* Accent & text */
  --loma-amber-light: #e8b04b;
  --loma-amber-mid: #d4942a;
  --loma-amber-dark: #c07f1a;
  --loma-amber-border: #a86a10;
  --loma-brick: #c0392b;
  --loma-brick-strong: #a2382c;
  --loma-text: #3a3a3a;
  --loma-text-body: #4a4a4a;
  --loma-text-muted: #736b60;
  --loma-text-on-canvas-muted: #625a4e;
  --loma-text-amber: #2c1b08;
  --loma-text-inverse: #f5f2ea;
  --loma-text-nav: #d8dde3;
  --loma-tag-text: #5a6a7a;
  --loma-focus: #28628a;

  /* Typography */
  --loma-font-ui: "Helvetica Neue", Helvetica, Arial,
    "PingFang SC", "Microsoft YaHei", "Noto Sans CJK SC", sans-serif;
  --loma-font-heading: Georgia, "Times New Roman", "Songti SC",
    "Noto Serif CJK SC", SimSun, serif;
  --loma-font-mono: "SFMono-Regular", Consolas,
    "Liberation Mono", monospace;

  /* Shape & layout */
  --loma-radius-sm: 4px;
  --loma-radius-button: 5px;
  --loma-radius-card: 6px;
  --loma-radius-tag: 12px;
  --loma-container: 960px;
  --loma-side: 280px;
  --loma-gap: 24px;

  /* Gradients */
  --loma-frame: linear-gradient(to bottom,
    var(--loma-slate-light) 0%, var(--loma-slate-mid) 50%,
    var(--loma-slate-dark) 100%);
  --loma-primary: linear-gradient(to bottom,
    var(--loma-amber-light) 0%, var(--loma-amber-mid) 50%,
    var(--loma-amber-dark) 100%);
  --loma-primary-pressed: linear-gradient(to bottom,
    var(--loma-amber-dark) 0%, var(--loma-amber-mid) 50%,
    var(--loma-amber-light) 100%);
  --loma-secondary: linear-gradient(to bottom,
    #fdfcf9 0%, #f0ece3 55%, #e1dbd0 100%);

  /* Elevation */
  --loma-shadow-card: 0 1px 3px rgb(0 0 0 / 8%),
    0 4px 12px rgb(0 0 0 / 5%);
  --loma-shadow-button: inset 0 1px 0 rgb(255 255 255 / 40%),
    0 1px 2px rgb(0 0 0 / 20%);
  --loma-shadow-frame: inset 0 1px 0 rgb(255 255 255 / 15%),
    0 2px 4px rgb(0 0 0 / 20%);
  --loma-shadow-overlay: 0 1px 2px rgb(0 0 0 / 15%),
    0 6px 18px rgb(0 0 0 / 12%);
  --loma-shadow-inset: inset 0 1px 3px rgb(0 0 0 / 12%);
  --loma-shadow-pressed: inset 0 2px 4px rgb(0 0 0 / 25%);

  --loma-transition-fast: 150ms;
  --loma-transition-normal: 200ms;
}

.loma-canvas {
  background-color: var(--loma-canvas);
  background-image:
    radial-gradient(circle at 20% 30%, rgb(255 255 255 / 60%) 0%, transparent 40%),
    radial-gradient(circle at 80% 70%, rgb(255 255 255 / 40%) 0%, transparent 35%),
    repeating-linear-gradient(
      45deg, rgb(0 0 0 / 1.2%) 0 1px, transparent 1px 6px
    );
}
