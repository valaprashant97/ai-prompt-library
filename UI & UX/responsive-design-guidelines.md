# Responsive Design Guidelines

```text
Responsive Design

Goal: Build interfaces that automatically adapt to different screen sizes, orientations, and available space while preserving usability, readability, visual hierarchy, performance, and design consistency.

Screen Coverage & Breakpoints
- Design every screen to work correctly across screen sizes, aspect ratios, and orientations — small, medium, large, and extra-large, where applicable.
- Do not assume a fixed screen width/height, and do not build layouts that depend on specific device dimensions.
- Use breakpoints only where a genuinely different layout is needed (e.g., switching multi-column to single-column).

Layout Adaptability
- Use flexible layouts that adapt to available space, changing layout structure — not just shrinking everything — as width changes.
- Ensure buttons, cards, lists, forms, and other components resize or reposition correctly at every size.
- Reuse the same components across screen sizes, letting their layout adapt to available space, instead of creating duplicated screens per size unless absolutely necessary.

Sizing & Scaling
- Dynamically scale text/typography size, spacing, margins, padding, icon size, button size, card dimensions, and other UI properties based on available screen/window size — across mobile, tablet, laptop, desktop, and large/ultra-wide screens.
- Avoid hardcoded widths, heights, and other fixed sizing wherever responsive sizing is appropriate; use fixed values only when genuinely required.
- Scale images, icons, and charts appropriately with the surrounding layout.

Text & Content Handling
- Prevent text overflow, clipping, and overlapping UI elements.
- Handle long text gracefully via wrapping, truncation, or adaptive layout.

Navigation & Accessibility
- Keep navigation usable on both small and large screens.
- Maintain proper alignment, spacing, and visual hierarchy across all screen sizes.
- Keep interactive elements accessible with adequate touch targets.

Platform & System UI
- Handle safe areas, system bars, notches, and display cutouts correctly.
- Support different device orientations where applicable.

Implementation & Testing
- Fix responsive issues at the layout level instead of using device-specific hacks.
- Test every important screen at multiple screen sizes before considering it complete.
```
