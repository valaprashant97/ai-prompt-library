# AI-Generated UI Tells Audit Prompt

## When to Use

Use this prompt when you want an AI coding tool to audit your UI for
common **AI-generated design tells** and fix them directly in the code.

It is especially useful when:

- Your landing page or app UI looks generic or "made by AI".
- You want a consistent, deliberate visual identity.
- You need a clean pass over color, typography, layout, copy and trust
  elements before launch.
- You want a checklist-style report of what was fixed and what needs
  your input.

## Prompt
Check my UI for these common AI-generated tells, and fix or replace them where appropriate:

1. Harsh gradients
2. Pure white backgrounds
3. Rainbow coloring
4. Heavy drop shadows
5. Liquid glass effects
6. Purple and black color schemes
7. Radial orbs
8. Neon colors
9. Basic pastel colors
10. Default Lucide icons
11. Emojis used as icons
12. Default Inter / Geist / Space Grotesk fonts
13. Sparkle icons
14. Animated arrows
15. Hover animations on everything
16. Three feature cards in a row
17. Colored left stripes on cards
18. Bento grids
19. Terminal window mockups
20. Three pricing tiers
21. Generic soft rounded corners
22. Dot grid backgrounds
23. Em dashes
24. "It's not X, it's Y" copy
25. Checkmark bullet lists
26. Fake testimonials
27. Missing real product demos
28. Missing skeleton loaders
29. Missing Terms of Service
30. Missing Privacy Policy

## Short Description

This prompt instructs an AI coding tool to scan the project for 30
common AI-design tells (gradients, pure white backgrounds, default
fonts, bento grids, fake testimonials, missing legal pages and more),
fix them in code, and return a clear report, while preserving the
existing layout, content structure and functionality.


## Prompt

```text
You are a senior product designer and front-end engineer. Audit the UI
in this project for common AI-generated design tells, then fix them
directly in the code. Do not just report issues. Make the changes,
keeping the product's layout, content structure and functionality
intact.

PROCESS
1. Scan all UI files (components, pages, styles, theme/config, copy,
   assets).
2. For each item below, record where it appears (file and line) or mark
   it "not found".
3. Fix every instance where it hurts the design. If an instance is
   intentional and works, leave it and say why.
4. Finish with a short report: what you changed, what you left alone
   and why, and anything that needs my input (real content, legal text,
   product screenshots).

Do not introduce a new tell while fixing another. For example, do not
swap a purple gradient for a teal one, or replace Inter with Space
Grotesk.

COLOR AND SURFACE
1. Harsh gradients: Remove high-contrast or multi-stop gradients. Use
   flat fills. If a gradient is justified, keep it to two close hues
   with low contrast.
2. Pure white backgrounds: Replace #fff with a warm or cool off-white
   tied to the brand hue. Do the same for pure black in dark mode (use
   a tinted near-black).
3. Rainbow coloring: Limit the palette to one primary hue, one accent,
   and neutrals. Semantic colors (error, success) are the only
   exception.
4. Heavy drop shadows: Replace large, dark, blurry shadows with a 1px
   border or a very subtle, low-opacity, tightly spread shadow.
5. Liquid glass effects: Remove heavy backdrop-blur, translucent frosted
   panels and glossy highlights. Use solid surfaces.
6. Purple and black color schemes: Replace the purple-on-black default
   with a palette derived from the product's actual brand or domain.
7. Radial orbs: Remove blurred glowing circles and aurora blobs behind
   hero sections.
8. Neon colors: Replace saturated glow colors with muted, accessible
   tones that meet WCAG AA contrast.
9. Basic pastel colors: Replace generic baby-blue, mint and lavender
   fills with deliberate, slightly desaturated tones that have a clear
   role in the palette.

TYPOGRAPHY AND ICONS
10. Default Lucide icons: Replace with a more distinctive icon set, or
    custom or lightly modified icons at consistent stroke weight.
    Remove icons that add no meaning.
11. Emojis used as icons: Replace with proper SVG icons or remove them.
12. Default Inter / Geist / Space Grotesk: Choose a considered pairing
    (a distinctive display face plus a readable text face) suited to
    the product's tone. Set a clear type scale, line heights and
    tracking.
13. Sparkle icons: Remove sparkle and magic-wand icons used to signal
    "AI". Label the feature plainly instead.

MOTION
14. Animated arrows: Remove arrows that slide or bounce on hover. Use a
    static arrow or none.
15. Hover animations on everything: Keep hover feedback only on
    interactive elements, and keep it subtle (color or underline
    change). Remove scale, lift and glow effects on cards, images and
    text. Respect prefers-reduced-motion.

LAYOUT AND SHAPE
16. Three feature cards in a row: Restructure the section. Use an
    alternating split layout, a single focused feature with a real
    visual, or a plain list with varied emphasis.
17. Colored left stripes on cards: Remove the accent border-left. Use
    spacing, type hierarchy or a small label to signal category or
    status.
18. Bento grids: Replace with a simpler, purposeful layout with a clear
    reading order.
19. Terminal window mockups: Remove fake terminal chrome (three dots,
    dark box, typed commands) unless the product is genuinely a CLI.
    Show the real product instead.
20. Three pricing tiers: Structure pricing around how the product is
    actually sold. Two options, a single price, usage-based, or
    "contact us" are all fine if true. Do not force three tiers with a
    highlighted middle plan.
21. Generic soft rounded corners: Replace uniform large radii (12 to
    24px on everything) with a deliberate radius system. Use sharper
    corners, or vary radius by element type.
22. Dot grid backgrounds: Remove dotted and grid-line backgrounds. Use
    a flat or subtly tinted background.

COPY
23. Em dashes: Replace with periods, commas, colons or parentheses.
    Rewrite the sentence if needed.
24. "It's not X, it's Y" copy: Rewrite as a direct statement of what the
    product does. Also remove similar patterns ("More than just...",
    "Not just X, but Y").
25. Checkmark bullet lists: Replace with plain prose, a normal list
    without check icons, or a table when comparing.
26. Fake testimonials: Delete invented quotes, names, avatars, logos
    and metrics. Replace with real ones if I provide them. Otherwise
    remove the section and leave a clearly marked TODO. Do not
    fabricate anything.

PRODUCT AND TRUST
27. Missing real product demos: Where the page describes the product,
    add or reserve a slot for a real screenshot, screen recording or
    interactive demo of the actual product. If none exists, add a
    labeled placeholder and list it in the report. Do not draw a fake
    UI.
28. Missing skeleton loaders: Add skeleton states that match the final
    layout for every async or data-driven view (lists, cards, tables,
    images). Use a subtle, non-flashy shimmer or a static placeholder,
    and respect reduced motion.
29. Missing Terms of Service: Add a /terms page and link it from the
    footer and any signup flow. Do not invent legal terms. Use a
    clearly marked draft template and flag that it needs legal review.
30. Missing Privacy Policy: Add a /privacy page and link it from the
    footer and any form that collects data. Same rule: marked draft,
    based on what the app actually collects, flagged for legal review.

OUTPUT
- Apply the edits to the code.
- Then give a checklist report with all 30 items, each marked Fixed,
  Kept (with reason), Not found, or Needs input.
- Keep the report plain. No emojis, no em dashes, no checkmark icons.
```
