# LoMA — Retro-Skeuomorphic Visual Design Language

> **Warm surfaces · Tactile controls · Editorial clarity**
> *(有温度的界面，可感知的材质，可理解的秩序。)*

| Document Property | Details |
| --- | --- |
| Name | LoMA |
| Document Type | Visual Design Language / UI Theme Specification |
| Version | 1.0.0 (Initial Draft) |
| Date | 2026-11-26 |
| Style Positioning | Restrained Skeuomorphism · Early Web 2.0 · Retro Editorial Typography |
| Scope | Websites, content platforms, desktop applications, utility WebUIs, game menus, and codex/encyclopedia interfaces |
| Reference Blueprint | `deepseek_html_20261126_c60833.html` (Pixel Journal) |

This document defines the visual grammar of LoMA rather than prescribing a rigid website template. All products adopting LoMA must maintain consistency across color, materiality, lighting, borders, typography, and interactive feedback; content, layout, and branding may vary according to the specific product.

**Normative Terminology:** **"Must"** indicates mandatory rules required to preserve style integrity or usability; **"Should"** indicates recommended defaults; **"May"** indicates permissible adjustments that do not violate core principles.

---

## 1. Design Philosophy

Taking inspiration from the gradients, inner highlights, hairline borders, paper textures, and editorial layouts common on the web circa 2010, LoMA restores a measured sense of physicality to modern interfaces. Rather than pursuing pixel-for-pixel imitation of real-world objects or turning every UI element into a 3D prop, it uses material cues to establish spatial relationships and authentic, restrained feedback to build operational intuition.

### 1.1 Core Principles

| Principle | Design Requirements |
| --- | --- |
| **Material Honesty** | Backgrounds feel like paper, content surfaces like cardstock, navigation chrome like dark painted metal, and controls like tangible physical parts. Materiality shifts with function. |
| **Tactile Affordance** | Pressable elements feature elevation, top highlights, and bottom edge shadows, depressingly inward with realistic feedback when activated. Non-interactive content layers never masquerade as buttons. |
| **Editorial Order** | Uses serif headings, clear column grids, hairline dividers, and compact yet breathable information structures—evoking a well-typeset magazine. |
| **Restrained Ornament** | Ornamentation must serve hierarchy. Textures remain low-contrast and shadows short and soft so lighting effects never overpower content. |
| **Modern Usability** | Retro aesthetics do not justify archaic interaction limits. Keyboard navigation, accessible states, mobile ergonomics, and clear reading contrast must be preserved. |

### 1.2 Style Boundaries

LoMA is a **light-to-moderate skeuomorphic** visual language:

* **Not pure flat design:** Key interactive controls must not be reduced entirely to borderless, solid-color rectangles.
* **Not heavy skeuomorphism:** Avoids large expanses of leather, woodgrain, rivets, analog gauges, or heavy photographic textures as default decoration.
* **Not glassmorphism:** Does not rely on backdrop blurs, translucent glass, or neon outlines as primary hierarchy mechanisms.
* **Not neumorphism:** Does not construct all controls solely via dual-direction shadows matching the background color; clear, recognizable borders must be preserved.
* **Not a nostalgia filter:** Does not simulate age through scanlines, distortion, distressed stains, or low-resolution artifacts.

## 2. Blueprint Feature Extraction

The values below are extracted directly from the reference HTML's CSS; subsequent sections abstract them into general design rules with modern extensions where necessary.

| Original Feature | Blueprint Parameters | LoMA Grammar |
| --- | --- | --- |
| Paper Base Color | `#E8E4DC`, dual radial soft glows and 45° fine hatch lines | Warm neutral canvas; texture remains subtler than content |
| Dark Navigation | `#4A5A6A → #35424F → #2B3642` | Cool-toned structural chrome, top highlight edge, bottom drop shadow |
| Cards | `#FDFCF9`, 1px warm gray border, 6px border radius | Paper-like content surface with subtle elevation |
| Primary Button | `#E8B04B → #D4942A → #C07F1A` | Molded amber physical piece with inner highlight and pressed inset |
| Links | `#C0392B` | Brick-red accent for clickable text |
| Typography | Georgia headings; Helvetica / Arial body | Serif for editorial voice and branding; sans-serif for functional readability |
| Content Width | 960px; 24px column gap; 280px sidebar | Centered regular grid with clear primary/secondary narrative structure |
| Lists | 14px vertical spacing, dashed dividers | Index-style information organization with clear horizontal rhythm |
| Border Radius | 5px buttons, 6px cards, 12px tags | Small radii for standard physical parts; pills reserved for tags and special badges |
| Transitions | 150–200ms | Brisk, localized, state-linked transitions |

**Retained Visual Signature:** Warm paper base + cool slate-blue chrome + amber controls + hairline borders + directional top-down lighting + serif headings. Even in interfaces without hero imagery, these traits should keep LoMA immediately recognizable.

## 3. Color System

### 3.1 Base Palette

The default theme is a warm light theme; values below are sRGB hex codes. Brand accent colors are part of the material system and do not need to appear on every component.

| Token | Color | Usage |
| --- | --- | --- |
| `canvas` | `#E8E4DC` | Global warm paper background |
| `canvas-deep` | `#DDD8CE` | Footers, lower background edges, secondary zones |
| `surface` | `#FDFCF9` | Cards, body containers, modal content surfaces |
| `surface-muted` | `#F0ECE3` | Tag backgrounds, secondary panels |
| `border` | `#D6D0C4` | Warm gray structural borders |
| `divider` | `#E3DDD1` | Hairline content dividers |
| `divider-dashed` | `#DDD6C8` | Dashed list dividers |
| `slate-light` | `#4A5A6A` | Dark chrome highlight |
| `slate-mid` | `#35424F` | Dark chrome midtone |
| `slate-dark` | `#2B3642` | Dark chrome shadow, heading text |
| `slate-border` | `#1E262E` | Dark chrome outer edge |
| `amber-light` | `#E8B04B` | Primary control and brand highlight |
| `amber-mid` | `#D4942A` | Primary control midtone |
| `amber-dark` | `#C07F1A` | Primary control shadow |
| `amber-border` | `#A86A10` | Primary control border |
| `brick` | `#C0392B` | Links, text emphasis |
| `brick-strong` | `#A2382C` | High-contrast links on warm paper backgrounds |
| `text` | `#3A3A3A` | Default body text |
| `text-body` | `#4A4A4A` | Card body text |
| `text-muted` | `#736B60` | Metadata on light card surfaces |
| `text-on-canvas-muted` | `#625A4E` | Small text on warm paper canvas and footers |
| `text-amber` | `#2C1B08` | Dark label text on amber buttons |
| `text-inverse` | `#F5F2EA` | Text on dark chrome |
| `text-nav` | `#D8DDE3` | Navigation item text |
| `tag-text` | `#5A6A7A` | Text on light tags |
| `focus` | `#28628A` | Keyboard focus ring |

### 3.2 Color Usage Rules

* Structure relies predominantly on warm neutrals; deep slate-blue is used for navigation, window title bars, toolbars, and primary headings.
* Amber is the **interactive accent color** and should be allocated first to primary actions, key active selections, or small brand marks.
* Brick red is the **textual accent color** suitable for links, though error states must always combine color with text or icons rather than relying on color alone.
* Recommended visual area proportions: 70–85% warm neutrals, 10–20% slate-blue chrome, and 3–10% accent colors. These serve as holistic interface guidelines rather than rigid quotas.
* Do not add high-saturation gradients, colored borders, or arbitrary color strips to every card.
* While the original HTML used `#9A9286` for light metadata and white text on amber buttons as period touches, LoMA drops both low-contrast pairings by default in favor of the high-contrast tokens listed above.

### 3.3 Functional Colors (Extended)

| State | Foreground | Subtle Background | Presentation |
| --- | --- | --- | --- |
| Success | `#35664E` | `#E8F0E6` | Checkmark icon + status text |
| Info | `#345E80` | `#E7EDF3` | Info icon + description |
| Warning | `#79500D` | `#F5EAD2` | Warning icon + remediation tip |
| Error | `#A2382C` | `#F6E5DF` | Error icon + specific cause |

Functional colors should be used primarily for compact badges and notifications rather than overriding the system's baseline material palette.

## 4. Materiality, Lighting & Space

### 4.1 Material Roles

| Material | Interface Role | Visual Execution |
| --- | --- | --- |
| Paper | Page canvas | Subtle paper grain, soft diffuse lighting, no heavy borders |
| Cardstock | Content cards, reference panels | Off-white tone, hairline warm gray border, short soft drop shadow |
| Coated Metal | Navigation, control chrome | Vertical slate-blue gradient, 1px top inner highlight, dark bottom edge |
| Molded Enamel / Soft Plastic | Buttons, interactive controls | Tonal gradient, inner highlight, defined border, and depressed state |
| Recess | Inputs, search bars, progress tracks | Subtle inner shadow with a stable outer border |
| Image Print | Covers, hero banners, media content | Natural tonal preservation, crisp edge cropping, and legible title scrims where needed |

Each component should use only one primary material, with at most one informational overlay layer. Materiality serves as a visual metaphor and does not require physically based rendering (PBR).

### 4.2 Lighting Model

* The default light source sits **directly overhead and slightly to the left**; light and shadow across all physical elements must remain consistent.
* **Raised elements:** Lighter on top, darker at the bottom; 1px inner top highlight; drop shadows cast primarily downward.
* **Recessed elements:** Inner shadow along the top edge, lighter interior; never combine with prominent outward drop shadows.
* Cards have only gentle elevation and must not feature strong surface gradients like buttons.
* Text shadows are reserved for dark navigation bars, brand titles, or text overlaid on imagery (`0 1px 1px rgba(0,0,0,.45)` recommended); never apply text shadows to body copy.
* Do not create inconsistent depth using multi-directional colored light sources, heavy white specular highlights, or large glossy reflections.

### 4.3 Gradients

| Usage | Specification |
| --- | --- |
| Dark Chrome | Top-to-bottom, `#4A5A6A 0%, #35424F 50%, #2B3642 100%` |
| Amber Button | Top-to-bottom, `#E8B04B 0%, #D4942A 50%, #C07F1A 100%` |
| Secondary Control | Top-to-bottom, `#FDFCF9 0%, #F0ECE3 55%, #E1DBD0 100%` |
| Footer | Top-to-bottom, `#E8E4DC → #DDD8CE` |
| Image Scrim | Bottom-to-top from translucent dark to transparent; ensure adequate contrast behind actual text areas |

Two to three color stops are sufficient to convey volume on controls; avoid harsh banding or excessive gloss. Gradient direction may invert to indicate a pressed state, but should not shift purely for decoration.

### 4.4 Paper Micro-Texture

The texture from the reference webpage can be reproduced directly in CSS, keeping the solid base color as a fallback:

```css
.loma-canvas {
  background-color: var(--loma-canvas);
  background-image:
    radial-gradient(circle at 20% 30%, rgb(255 255 255 / 60%) 0%, transparent 40%),
    radial-gradient(circle at 80% 70%, rgb(255 255 255 / 40%) 0%, transparent 35%),
    repeating-linear-gradient(
      45deg, rgb(0 0 0 / 1.2%) 0 1px, transparent 1px 6px
    );
}

```

Textures must never interfere with Latin or CJK character strokes, small text, form fields, or icons; avoid repeating diagonal hatch lines across individual cards or buttons. Keep large-area texture opacity low and offer a texture-free mode if needed.

### 4.5 Elevation & Shadow Levels

| Level | CSS Shadow | Usage |
| --- | --- | --- |
| E0 · Base | `none` | Paper surfaces, text, standard dividers |
| E1 · Cardstock | `0 1px 3px rgb(0 0 0 / 8%), 0 4px 12px rgb(0 0 0 / 5%)` | Cards, static panels |
| E2 · Control | `inset 0 1px 0 rgb(255 255 255 / 40%), 0 1px 2px rgb(0 0 0 / 20%)` | Buttons, raised controls |
| E3 · Chrome | `inset 0 1px 0 rgb(255 255 255 / 15%), 0 2px 4px rgb(0 0 0 / 20%)` | Top bars, fixed toolbars |
| E4 · Overlay | `0 1px 2px rgb(0 0 0 / 15%), 0 6px 18px rgb(0 0 0 / 12%)` | Hero banners, menus, popovers |
| I1 · Inset | `inset 0 1px 3px rgb(0 0 0 / 12%)` | Inputs and recessed tracks |
| I2 · Pressed | `inset 0 2px 4px rgb(0 0 0 / 25%)` | Actively pressed buttons |

Elevation levels correspond to functional roles and spatial placement rather than a strict hierarchy of shadow darkness. Modals may extend E4's spread radius, but avoid stacking multiple heavy shadow layers within a single view.

## 5. Geometry System

* **Base Stroke:** 1 CSS px. Content borders may remain low-contrast; form fields, focus states, and interactive boundaries must remain clearly legible.
* **Standard Corner Radius:** 4–6px. Large content containers should avoid oversized modern card radii.
* **Component Radii:** 4px for small controls; 5px for buttons; 6px for standard cards, hero banners, and dialogs.
* **Tag Radius:** 12px or half the control height; pill shapes are not the default for general buttons.
* **Circular Controls:** Reserved strictly for elements with explicit circular affordances such as avatars, icon buttons, and status indicators.
* **Focus Ring:** 2px solid outline with a 2px outer offset; use a light-colored ring on dark surfaces while maintaining sufficient contrast.
* Excessive corner chamfering, multiple decorative borders on a single component, and non-functional skewed shapes are prohibited.

## 6. Typography

### 6.1 Font Stacks

```css
--loma-font-ui: "Helvetica Neue", Helvetica, Arial, "PingFang SC",
  "Microsoft YaHei", "Noto Sans CJK SC", sans-serif;
--loma-font-heading: Georgia, "Times New Roman", "Songti SC",
  "Noto Serif CJK SC", SimSun, serif;
--loma-font-mono: "SFMono-Regular", Consolas, "Liberation Mono", monospace;

```

Serifs are used for brand wordmarks, article titles, and section headings; sans-serifs are used for body copy, navigation, and UI controls. CJK headings must include appropriate Songti/Mincho fallbacks to prevent jarring stylistic mismatches between Latin Georgia and default CJK sans-serif fonts. Monospace fonts may be used for telemetry, code, and serial numbers, but not for general prose.

### 6.2 Type Scale

| Role | Size | Line Height | Weight / Family |
| --- | --- | --- | --- |
| H1 / Hero Title | 30px | 1.25 | 700, Serif |
| Page Title / Brand | 22–26px | 1.3 | 700, Serif |
| H2 / Card Title | 20px | 1.35 | 700, Serif |
| H3 / Widget Title | 16px | 1.4 | 700, Serif |
| List Item Title | 16px | 1.45 | 600–700, Serif |
| Body Text | 14px | 1.6 | 400, Sans-serif |
| Long-Form Reading (Extended) | 15–16px | 1.7–1.85 | 400, Sans-serif |
| Navigation, Buttons | 13–14px | 1.4–1.5 | 400 / 600–700, Sans-serif |
| Metadata, Tags, Footer | 12–13px | 1.5 | 400, Sans-serif |

* Default headings use dark slate-blue (`slate-dark`) and body text uses warm charcoal (`text`); avoid setting entire pages in pure `#000` or `#FFF`.
* Latin headings may use approximately `0.5px` letter-spacing; CJK body text uses no extra letter-spacing by default.
* Supporting metadata such as dates and authors may use subtle italics in Latin scripts; avoid forcing synthetic italics on CJK text.
* Content headings should convey hierarchy primarily through type scale, weight, and hairline dividers rather than abrupt size jumps.
* UI font sizes should be implemented in `rem` or scalable equivalents; `12px` is the default minimum visual size, and user text zoom must never be restricted.

## 7. Spacing, Layout & Responsiveness

### 7.1 Spacing

Construct spacing scales on a 4px base grid while preserving optical refinements from the blueprint (such as 6px, 10px, 14px, and 22px) suited to editorial typography.

| Step | Default Value | Use Cases |
| --- | --- | --- |
| XS | 4–6px | Between tags, headings and metadata |
| S | 8–12px | Button padding, compact widgets |
| M | 14–16px | Content paragraphs, list rows |
| L | 20–24px | Card padding, column gaps |
| XL | 28–32px | Major sections, hero-to-content spacing |
| XXL | 40px | Main container bottom clearance |

### 7.2 Grid

Content-driven pages default to a **centered magazine-style container**, while utility interfaces may adopt viewport-adaptive panel layouts.

| Parameter | Default Value |
| --- | --- |
| Max Outer Container Width | 960px (including horizontal padding, matching source) |
| Container Horizontal Padding | 20px |
| Container Top / Bottom Padding | 28px / 40px |
| Navigation Height | 52px |
| Main-to-Sidebar Gap | 24px |
| Sidebar Width | 280px |
| Card Padding | 22px 24px |
| Card Vertical Gap | 22px |
| Hero Banner Reference Height | 300px |

Desktop two-column layout diagram (at max container width):

```text
┌─────────────────── Slate-Blue Top Bar ───────────────────┐
│ Brand                                         Navigation │
└──────────────────────────────────────────────────────────┘
       ┌─────────────────── Hero ───────────────────┐
       │                            Image + Title   │
       └────────────────────────────────────────────┘
       ┌────────────────────────┐  ┌────────────────┐
       │ Main Content 616px     │  │ Sidebar 280px  │
       │ Articles, Lists, Tools │  │ Categories     │
       └────────────────────────┘  └────────────────┘
                      24px Column Gap

```

Layout widths may adapt to product needs—for example, data-dense utility tools may expand to 1200px or use fluid workspaces—provided consistent spacing, primary/secondary hierarchy, structural borders, and reading rhythm are maintained.

### 7.3 Responsiveness

* **Above 760px:** Default two-column layout; main column flexes while sidebar remains fixed at ~280px.
* **760px and below:** Collapses to a single column; sidebar moves completely below the main column; hero title scales to ~22px.
* On narrow viewports, outer container padding may tighten to 12–16px and card padding to 16px.
* Mobile navigation must convert into an expandable drawer or accessible compact menu—never hidden outright without an alternative trigger as in the raw blueprint.
* Interactive targets on touch devices should measure at least 44×44px; smaller visual controls may expand their hit areas without overlapping adjacent targets.
* Standard pages must not trigger viewport-wide horizontal scrolling at 320 CSS px width or under text zoom. Wide data tables may scroll independently within their own containers.

## 8. Component Specifications

### 8.1 Navigation Bar & Application Toolbar

* Uses the three-stop vertical slate-blue gradient, a 1px dark bottom border, a top inner highlight, and E3 elevation.
* Brand wordmarks use warm off-white serif type; any amber accents should remain compact and legible, shifting to a lighter high-contrast shade if used for essential text.
* Navigation links are 13–14px with a 4px radius and light gray text at rest, gaining a low-opacity light fill on hover.
* Active items use a solid fill or recessed well paired with a clear indicator (such as bold weight or an underline bar); never rely on hover styles alone to mark the current page.
* Fixed top bars must leave sufficient scroll margin so keyboard-focused elements are never obscured.

### 8.2 Content Card

* Solid warm-white fill (`surface`), 1px `border`, 6px radius, and E1 elevation; no full-card gradients by default.
* Card headers are separated from body content by a 1px warm gray solid rule; metadata such as dates, authors, or categories sits directly beneath the heading.
* Cards at the same hierarchical level share identical borders, padding, and shadows. Static cards must not exhibit clickable hover transitions.
* List-style cards may omit individual row backgrounds and use hairline dividers to organize dense entries.

### 8.3 Buttons

| Variant | Surface | Semantics |
| --- | --- | --- |
| Primary | Three-stop amber gradient, dark label text, dark amber border | Primary action on the page or in a workflow |
| Secondary | Light warm gray gradient, slate-blue text, dark warm gray border | Secondary actions |
| Quiet | Transparent or low-contrast fill while keeping text affordance clear | Low-priority or toolbar actions |
| Destructive | Deep brick-red gradient (e.g., `#A2382C → #83291F`), light label text | Irreversible actions such as deletion; pair with explicit verbs |

Default compact buttons use 13–14px type at 600–700 weight, 18px horizontal padding, 8px vertical padding, and a 36px minimum height (expanded to 44px on touch devices). Not all clickable text needs to be styled as a raised button.

| State | Feedback |
| --- | --- |
| Rest | Lighter top, darker bottom, E2 shadow, crisp border |
| Hover | Slightly brightened surface, preserved border, ~150ms transition |
| Focus-visible | 2px high-contrast focus ring without overlapping the button label |
| Active / Pressed | Inverted or flattened gradient, I2 inner shadow, outer drop shadow removed |
| Disabled | Low-saturation warm gray surface, no specular highlight; label and reason remain legible |
| Loading | Preserves button dimensions, displays progress text or subtle spinner, prevents duplicate submission |

Pressing a button must never cause neighboring layout shifts. Focus, selected, hover, and pressed states are distinct and must not be conflated.

### 8.4 Forms (Input / Select / Textarea)

The original blueprint lacked complete form controls; LoMA extends its material grammar to cover them:

* Input fields use a warm-white surface, 4–5px radius, clear warm gray border, and I1 inner shadow to convey a recessed well.
* Minimum height is 36px (at least 44px touch hit target). Visible labels sit above or beside fields; placeholders must never replace labels.
* Select triggers inherit the secondary button material; dropdown menus use warm-white cardstock with E4 elevation.
* Focused inputs display the standard focus ring; validation errors combine a brick-red border, error message, and icon.
* Placeholder text must be legible without overpowering actual user input.
* Checkboxes and radio buttons feature crisp borders and clear check/dot fills; checked states may use amber fills with dark glyphs.

### 8.5 Tags, Lists & Tables

* **Tags:** Default to `surface-muted` with a 1px border, 12px radius, subtle 1px top inner highlight, 12–13px text, and ~3px 10px padding. Active or hovered tags may switch to an amber fill with dark text.
* **Lists:** Roughly 14px vertical spacing per item, separated by 1px dashed or solid hairlines, with outer margins trimmed on first and last items. Item titles may use 16px bold serif type.
* **Tables:** Use light warm gray headers, warm-white cell backgrounds, hairline rules, and subtle row striping; right-align numeric columns. Row action buttons should not visually dominate the table.
* **Tabs:** Tab bars use light warm gray framing, while the active tab connects seamlessly to the content pane via a warm-white surface or clear physical tab shape paired with proper ARIA selection states.

### 8.6 Hero Media

* Uses a 6px radius, clean edge cropping, a 1px low-contrast border, and E4 elevation.
* Hero banners may display photography, illustration, or a muted slate-to-umber gradient at a default height of ~300px.
* Overlaid headlines (~30px, white or warm off-white) sit over a dark bottom gradient scrim reinforced with a 1–2px text shadow.
* Always verify text contrast against the actual image. If a scrim is insufficient, add a solid title band or reposition the text rather than relying solely on text shadows.

### 8.7 Icons, Badges & Status Indicators

* Standard icons favor clean original line or solid glyphs built on a 16/20/24px grid with ~1.5–2px stroke weight.
* Standalone pressable icon buttons may use subtle gradients, 1px inner highlights, and short shadows; non-interactive icons remain flat.
* Badges, tags, and status indicators communicate via color, shape, and text together. Icon-only buttons must include accessible labels or clear tooltips.
* Do not mix chunky realistic icons, glossy orb icons, and ultra-thin hairlines; maintain a unified visual grammar within any icon set.

### 8.8 Dialogs, Notifications & Progress (Extended)

* **Dialogs:** Warm-white cardstock surface, 6px radius, E4 elevation, optional dark title chrome, and an amber primary action button. Backdrops should dim background distractions without relying on heavy blur effects.
* **Notifications:** Tinted surfaces derived from functional colors, conveying status through hairline borders, text, and icons without bouncy animations or flashing.
* **Progress Bars:** Light recessed track paired with an amber or slate-blue fill and optional subtle top highlight; indeterminate states require clear waiting indicators.
* **Tooltips & Menus:** Warm-white surfaces with crisp borders and short soft shadows (or dark slate-blue where appropriate); show and dismiss behaviors must support keyboard navigation.

### 8.9 Footer

Vertical warm gray gradient with a 1px top border and 12–13px muted text. The footer should feel like an extension of the paper canvas rather than an inverted copy of the dark top navigation bar.

## 9. Motion & Interactive Feedback

| Interaction | Duration | Rules |
| --- | --- | --- |
| Button color / lighting shift | 150ms | Brisk, zero delay |
| Navigation & tab backgrounds | 150–200ms | `ease-out` or `ease` timing |
| Menus & overlays | 120–200ms | Fade in with subtle translation (≤ 4px) |
| Icon hover | 150ms | May lift 1–2px without affecting layout |
| Active press | ~0–80ms | Prioritize immediate feedback; never block on animation completion |

Apply short transitions strictly to color, opacity, shadow, and minor translation; avoid unconstrained `transition: all`. Do not use prolonged spring physics, cursor-tracking spotlights, or continuous pulsing. Respect `prefers-reduced-motion` by disabling non-essential motion while keeping state changes intact, and never rely on animation as the sole indicator of state.

## 10. Web Implementation Reference

The following CSS serves as a modernized starting point distilled from the blueprint rather than a standalone page. Other platforms (such as Godot or desktop UI toolkits) can map these same token names to theme resources, StyleBoxes, gradient textures, and control states without mechanically replicating CSS shadow syntax.

### 10.1 Core Tokens

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

  /* Type */
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

  /* Surface gradients */
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

```

### 10.2 Base Component CSS

```css
*, *::before, *::after { box-sizing: border-box; }

body {
  margin: 0;
  font: 0.875rem/1.6 var(--loma-font-ui);
  color: var(--loma-text);
  background-color: var(--loma-canvas);
}
h1, h2, h3 {
  font-family: var(--loma-font-heading);
  color: var(--loma-slate-dark);
}
a { color: var(--loma-brick-strong); }
a:hover { text-decoration: underline; }

.loma-topbar {
  background: var(--loma-slate-mid);
  background-image: var(--loma-frame);
  color: var(--loma-text-inverse);
  border-bottom: 1px solid var(--loma-slate-border);
  box-shadow: var(--loma-shadow-frame);
}
.loma-topbar :is(h1, h2, h3) { color: inherit; }
.loma-topbar a { color: var(--loma-text-nav); }
.loma-container {
  max-width: var(--loma-container);
  margin-inline: auto;
  padding: 28px 20px 40px;
}
.loma-layout {
  display: grid;
  grid-template-columns: minmax(0, 1fr) var(--loma-side);
  gap: var(--loma-gap);
  align-items: start;
}
.loma-card {
  background: var(--loma-surface);
  border: 1px solid var(--loma-border);
  border-radius: var(--loma-radius-card);
  box-shadow: var(--loma-shadow-card);
  padding: 22px 24px;
}
.loma-card > h2 {
  margin: 0 0 8px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--loma-divider);
  font-size: 1.25rem;
}
.loma-meta {
  font-size: 0.75rem;
  color: var(--loma-text-muted); /* on surface */
}
.loma-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
  min-height: 36px;
  padding: 8px 18px;
  font: 700 0.8125rem/1.4 var(--loma-font-ui);
  text-decoration: none;
  color: var(--loma-text-amber);
  background: var(--loma-amber-light);
  background-image: var(--loma-primary);
  border: 1px solid var(--loma-amber-border);
  border-radius: var(--loma-radius-button);
  box-shadow: var(--loma-shadow-button);
  text-shadow: 0 1px 0 rgb(255 255 255 / 25%);
  cursor: pointer;
  transition: box-shadow var(--loma-transition-fast),
    border-color var(--loma-transition-fast);
}
.loma-button:hover:not(:disabled) {
  background-image: linear-gradient(to bottom,
    #f0bc58 0%, #dd9f36 50%, #c98a22 100%);
  text-decoration: none;
}
.loma-button:active:not(:disabled) {
  background-image: var(--loma-primary-pressed);
  box-shadow: var(--loma-shadow-pressed);
}
.loma-button--secondary {
  background: var(--loma-surface-muted);
  background-image: var(--loma-secondary);
  color: var(--loma-slate-dark);
  border-color: #8e8679;
}
.loma-button--secondary:hover:not(:disabled) {
  background-image: linear-gradient(to bottom, #fffefa, #e9e4da);
}
.loma-button--secondary:active:not(:disabled) {
  background-image: linear-gradient(to bottom, #e1dbd0, #fdfcf9);
}
.loma-button:disabled {
  background: #e2ded5;
  border-color: #b3aa9c;
  color: #625a4e;
  box-shadow: none;
  text-shadow: none;
  cursor: not-allowed;
}
.loma-input {
  min-height: 36px;
  max-width: 100%;
  padding: 8px 10px;
  font: inherit;
  color: var(--loma-text);
  background: var(--loma-surface);
  border: 1px solid #8e8679;
  border-radius: var(--loma-radius-sm);
  box-shadow: var(--loma-shadow-inset);
}
:focus-visible {
  outline: 2px solid var(--loma-focus);
  outline-offset: 2px;
}
.loma-topbar :focus-visible {
  outline-color: var(--loma-text-inverse);
}
@media (max-width: 760px) {
  .loma-layout { grid-template-columns: minmax(0, 1fr); }
  .loma-container { padding-inline: 16px; }
  .loma-card { padding: 16px; }
}
@media (pointer: coarse) {
  .loma-button, .loma-input { min-height: 44px; }
}
@media (prefers-reduced-motion: reduce) {
  .loma-button { transition: none; }
}

```

Components should prioritize semantic HTML (`<button>`, `<a>`, `<input>`, `<nav>`, `<main>`, etc.). CSS classes handle visual styling and do not replace state semantics or functional behavior. Never substitute an interactive element with a keyboard-inaccessible `<div>` solely for styling convenience.

## 11. Accessibility, Extension & Consistency

### 11.1 Usability Baselines

* Target a minimum contrast ratio of 4.5:1 for normal text and 3:1 for large text; essential non-text interactive boundaries and status indicators should achieve at least 3:1.
* Evaluate contrast on gradient surfaces against the worst-case color stop beneath the text rather than the average or lightest stop.
* Default verification examples: dark amber button text (`#2C1B08`) against the darkest gradient stop (`#C07F1A`) achieves ~4.96:1; card metadata (`#736B60`) on `surface` (`#FDFCF9`) achieves ~5.12:1.
* Never use low-contrast decorative dividers as the sole boundary for required form inputs.
* All interactive components must provide a visible focus indicator, accessible name, state semantics, and full keyboard operability; high-contrast / forced-colors modes must allow system color overrides.
* Information must never be conveyed solely through gradient direction, shadows, color, or texture; icons and text must carry explicit semantic meaning.
* Verify every theme variant, background image, text pairing, and interactive state in real projects; the palette in this specification does not guarantee contrast compliance across arbitrary combinations.

### 11.2 Extension Strategy

* When creating new components, define their semantic role first, match them to the appropriate material, geometry, color tokens, and elevation level, and finally specify their static and interactive states.
* Brand theming may swap out the amber accent color, provided the primary-to-secondary hierarchy between warm paper and dark chrome is preserved and contrast ratios are re-verified.
* A dark mode is not included as an out-of-the-box mapping in this version. Any future dark variant of LoMA must redefine materiality, lighting, and text hierarchy from the ground up rather than inverting colors naively.
* LoMA can be applied to desktop software, game UIs, and utility tools without forcing the web's 960px two-column layout.
* New design tokens should carry semantic names, and existing components should reference established tokens rather than scattering one-off hardcoded hex values.

## 12. Design Acceptance Checklist

### Visual Consistency

* [ ] Clear hierarchy among the warm paper canvas, warm-white content surfaces, slate-blue chrome, and amber primary controls.
* [ ] Surface textures remain lower in contrast than body text, with no muddy smudges, heavy noise, or overly distressed effects.
* [ ] Clear distinction in font roles, type scale, and spacing between headings and body text.
* [ ] Crisp, consistent hairline borders and predominantly 4–6px corner radii.
* [ ] Unified top-down lighting direction across all highlights and shadows.
* [ ] Distinct visual feedback differentiating raised controls from recessed controls.
* [ ] Content surfaces remain restrained rather than styling every container with button-like gradients.

### Functionality & Usability

* [ ] Every interactive component supports rest, hover, focus, pressed, and (where applicable) disabled states.
* [ ] Text, essential boundaries, and status indicators meet target contrast ratios.
* [ ] Controls can be reached, operated, and dismissed via keyboard.
* [ ] Mobile navigation is complete, touch targets are adequately sized, and narrow screens avoid unintended page-wide horizontal scrolling.
* [ ] Non-essential animations can be disabled while keeping states clear.
* [ ] Content remains unclipped and hierarchical integrity holds under text zoom.

### Implementation & Maintenance

* [ ] Core colors, radii, spacing, shadows, and gradients are managed via theme tokens.
* [ ] Extended components adhere to the same semantic material system.
* [ ] No off-brand large-area backdrop blurs, neon glows, or oversized radii are introduced.
* [ ] Custom brand variants and live content undergo independent visual verification.

---

## 13. Design Language Overview

The essence of LoMA is not "making modern web pages look old," but restoring tangible materiality, crisp boundaries, clear hierarchy, and satisfying tactile feedback to digital interfaces. It carries information on paper, builds structure with deep slate-blue, and signals action in amber—uniting consistent lighting, restrained gradients, compact editorial typography, and disciplined detail to lend digital products physical order and human warmth.

> **LoMA: design with the warmth of paper and the precision of an instrument.**
> *(以纸张的温度、器物的精确，设计数字界面。)*
