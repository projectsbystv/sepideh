# cafe-amaya DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 5 · Fonts: 2 · Components: 7
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![cafe-amaya Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a cool tone. Depth is expressed through layered shadows and subtle surface color variation. Typography pairs **Sora** for display/headings with **Inter** for body text, creating clear visual hierarchy through type contrast. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 16, 24px. The palette is predominantly monochromatic with **#0080ff** as the single accent color — used sparingly for interactive elements and emphasis. Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| background | `#000000` | background | Page background, darkest surface |
| surface | `#07071a` | surface | Card and panel backgrounds |
| text-primary | `#ffffff` | text-primary | Headings and body text |
| accent | `#0080ff` | accent | CTAs, links, focus rings, active states |
| info | `#e9ecf6` | info | Informational highlights |

### CSS Variable Tokens

```css
--one-kit-border-width: 0px;
--one-kit-border-width: 1px;
--one-kit-atom-border-width: 1px;
--one-kit-container-border-width: 1px;
--one-kit-border-width: 0;
--one-kit-border-width: 1px;
--one-kit-border-width: 2px;
--one-kit-border-width: 3px;
--one-kit-border-width: 4px;
--one-kit-border-width: 5px;
--one-kit-atom-border-width: 0;
--one-kit-atom-border-width: 1px;
--one-kit-atom-border-width: 2px;
--one-kit-atom-border-width: 3px;
--one-kit-atom-border-width: 4px;
--one-kit-atom-border-width: 5px;
--one-kit-container-border-width: 0;
--one-kit-container-border-width: 1px;
--one-kit-container-border-width: 2px;
--one-kit-container-border-width: 3px;
```


---

## 3. Typography Rules

**Font Stack:**
- **Inter** — Heading 1, Heading 2, Heading 3
- **Sora** — Body, Caption

**Font Sources:**

```css
@font-face {
  font-family: "Sora";
  src: url("https://onecdn.io/font-storage/sora/sora-regular.woff2") format("woff2");
  font-weight: 400;
}
@font-face {
  font-family: "Sora";
  src: url("https://onecdn.io/font-storage/sora/sora-700.woff2") format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Inter";
  src: url("https://onecdn.io/font-storage/inter/inter-regular.woff2") format("woff2");
  font-weight: 400;
}
@font-face {
  font-family: "Inter";
  src: url("https://onecdn.io/font-storage/inter/inter-700.woff2") format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Xing";
  src: url("data:font/woff2;charset=utf-8;base64,d09GMgABAAAAAAJoAAsAAAAABcAAAAIdAAEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAHFQGVgCCcApAZAE2AiQDCAsGAAQgBYNmBzMbGAXIjgJ3BS3dYsj7F0Gw9r/Zs2+m8SdtYohINskkoiZCJRKhFEI1y2+/6S9/bIZH5eE7JWNt25G7zkvfNSxhwBgkSqMQEqUYOCdvTZIAGvnKwiiwA94OnOUFdKEDHfnD2AUu4RGBSvM2dNcPzu5g4XYkBpb0WdNBWh+3cx3BmEdkMlgoF4qac8/ihRzvvMdQ+PUH5qyCRJ6ymnav7qew9SXseQFtseY+yJFiGgCfOKz1bOvBzLSeSu1y3yCQyQRfolTybWKvZsH+Oqu2GnTDWPDFPSNAArJ4tgnoGnUbSUXlscfpIdxXVR3dCJ9H5cIhLDr2dW3rc9nZHfNHO8sLR/8+hvlPY6t+x/XBFhz76pdVfnLy8u/mucWV/+VVAT7//vAy5Pr5KN+LPrbG+3ZfIwkakhZN5HRNozYmqFSJEitQ72eq0ezUvjJZSqQyVUCG1BG5Kk1EIdNLVJqyzLauP9cTWYVQ7jwkErWuE6lyd4AMeULkWn0ohY68JSod9X2wyqj/4zeMviH9XEVWYd1FD2TbnA0Gs/PZTxySIRsJpRi/Y/uiQxGFynKNB2yEqoqxsVxQIm4m0qx4c1fr3nATruFJztBuEO1ZJWKZGAYfEAi025iBAi6/BTjUmFZmRJD03tg71HqhhYRQkOKVrIYOZmF7dlYqDDX1ywokIVzZiFRjhWdPUn09rmSWse6f6IbxJFpTFbdZs/N2VWYAAA==") format("woff2");
  font-weight: 400;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Inter | 26px | 700 |
| Heading 2 | Inter | 20px | 700 |
| Heading 3 | Inter | 18px | 700 |
| Body | Sora | var(--one-kit-size,16px) | 400 |
| Caption | Sora | var(--button-size,16px) | 400 |

**Typographic Rules:**
- Limit to 2 font families max per screen
- Use **Inter** for body/UI text, **Sora** for display/headings
- Maintain consistent hierarchy: no more than 3-4 font sizes per screen
- Headings use bold (600-700), body uses regular (400)
- Line height: 1.5 for body text, 1.2 for headings
- Use color and opacity for secondary hierarchy, not additional font sizes


---

## 4. Component Stylings

### Navigation (1)

**Navigation** — `html`

### Data Display (1)

**List** — `html`

### Data Input (1)

**Button** — `html`
- Animation: 

### Overlay (1)

**Modal** — `html`

### Media (3)

**Image** — `html`

**Icon** — `html`

**Map/Canvas** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 16, 24, 32, 36, 40, 80
- **Border radius:** 4px, 6px, 8px, 10px, 100px, unset
- **Max content width:** 992px

**Spacing as Meaning:**
| Spacing | Use |
|---|---|
| 4-8px | Tight: related items within a group |
| 12-16px | Medium: between groups |
| 24-32px | Wide: between sections |
| 48px+ | Vast: major section breaks |


---

## 6. Depth & Elevation

### Flat — subtle depth hints

- `0 0 0 var(--one-kit-border-width,0) rgba(var(--color-border),var(--alpha-border)),0 0 0 .1px rgba(var(--color-border),var(--alpha-border)) inset`

### Raised — cards, buttons, interactive elements

- `var(--one-kit-shadow)`
- `var(--one-kit-container-shadow)`
- `0 0 0 0 rgba(var(--color-bg),.4)`

### Floating — dropdowns, popovers, modals

- `0 0 0 20px rgba(var(--color-bg),0)`
- `0 0 0 15px rgba(var(--color-bg),0)`

### Overlay — full-screen overlays, top-level dialogs

- `8px 8px 40px rgba(0,0,0,.1)`

### Z-Index Scale

`0, 1, 2, 3, 5, 10, 20, 100, 500, 1000, 9999, 10000, 999999, 10000000`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes pulsate`
- `@keyframes pulsate-infinite`
- `@keyframes ripple-infinite`
- `@keyframes pulsate-ripple-infinite`
- `@keyframes pulsate-ripple-before-infinite`
- `@keyframes blink-infinite`
- `@keyframes hard-blink-infinite`
- `@keyframes bounce-infinite`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#0080ff` for interactive elements (buttons, links, focus rings)
- Use `#000000` as the primary page background
- Pair **Inter** (body) with **Sora** (display) — these are the only allowed fonts
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: 4px, 6px, 8px, 10px, 100px
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't introduce additional font families beyond Inter and Sora
- Don't use arbitrary spacing values — stick to multiples of 4px
- Don't create custom box-shadow values outside the system tokens
- Don't use arbitrary border-radius values — pick from the defined scale
- Don't duplicate component patterns — check Section 4 first
- Don't use backdrop-blur or blur effects

### Anti-Patterns (detected from codebase)

- No blur or backdrop-blur effects
- No zebra striping on tables/lists


---

## 9. Responsive Behavior

| Name | Value | Source |
|---|---|---|
| xs | 450px | css |
| md | 768px | css |
| lg | 992px | css |
| xl | 1200px | css |
| 2xl | 1366px | css |
| 2xl | 1440px | css |
| 2xl | 1600px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #07071a
Border: 1px solid var(--border)
Radius: 10px
Padding: 16px
Font: Inter
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg #0080ff, text white
Ghost: bg transparent, border var(--border)
Padding: 8px 16px
Radius: 10px
Hover: opacity 0.9 or lighter shade
Focus: ring with #0080ff
```

### Build a Page Layout

```
Background: #000000
Max-width: 992px, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #07071a
Label: var(--text-muted) (muted, 12px, uppercase)
Value: #ffffff (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #000000
Input border: 1px solid var(--border)
Focus: border-color #0080ff
Label: var(--text-muted) 12px
Spacing: 16px between fields
Radius: 10px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Inter, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```
