# Animated Skeleton Loading / Shimmer Loading Prompt

## When to Use

Use this prompt when you want to implement a professional, animated
Skeleton Loading / Shimmer Loading experience in any app or website.

It is suitable for: - Flutter applications - Web applications - Mobile
applications - Desktop applications - Dashboards - Social media feeds -
E-commerce applications - Chat applications - Profile screens - Tables
and lists - Any data-driven UI

------------------------------------------------------------------------

## Description

This prompt instructs an AI coding agent to implement a **real animated
Skeleton Loading / Shimmer Loading system**, similar to the loading
experience commonly used by modern popular applications and websites.

The skeleton should represent the actual content structure while data is
loading. A smooth shimmer highlight must continuously move across the
placeholders until the real content becomes available.

The implementation should be reusable, responsive, performant,
theme-aware, and should not cause layout shifting.

------------------------------------------------------------------------

## Prompt

``` text
Implement a professional, modern, production-ready Animated Skeleton Loading / Shimmer Loading system for this application/website.

The loading experience should follow the same general UX pattern used by modern popular applications and websites: show the structure of the real content immediately, then continuously animate a subtle shimmer/highlight across the placeholders until the real content is ready.

IMPORTANT:
This must be a REAL animated shimmer loading experience.
Do NOT create static gray placeholder boxes.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. SKELETON STRUCTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Before the actual content loads, display skeleton placeholders that accurately represent the final UI.

Create skeleton placeholders for whatever exists on the current screen, such as:

- Text
- Headings
- Paragraphs
- Avatars
- Profile images
- Images
- Videos/media thumbnails
- Cards
- Buttons
- Navigation items
- Lists
- Tables
- Form fields
- Charts
- Progress indicators
- Feed/post items
- Comments
- Product items
- Dashboard widgets
- Sidebar items
- Header elements

Do NOT use generic full-screen rectangles.

The skeleton must follow the actual content structure.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
2. REAL SHIMMER ANIMATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Every visible skeleton element must have a smooth animated shimmer effect.

The shimmer should behave like modern production applications:

- A soft highlight travels continuously across the skeleton.
- Direction: LEFT → RIGHT.
- The highlight moves smoothly across the entire placeholder.
- After reaching the right edge, it loops continuously from the left.
- Animation continues for the entire loading duration.
- The shimmer must be clearly visible but subtle.
- Do not use flashing or aggressive animations.

Visual concept:

BASE ─────────────────────
      ░░░░ LIGHT SHIMMER ░░
              → → → → →

The highlight must physically MOVE across the skeleton.

A static gradient is NOT acceptable.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
3. ANIMATION IMPLEMENTATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Use the platform/framework's proper animation system.

For Flutter, use an efficient implementation such as:

- AnimationController
- repeat()
- AnimatedBuilder
- LinearGradient
- GradientTransform / Transform.translate
- efficient reusable shimmer widget

For Web, use an equivalent CSS/JS animation approach such as:

- linear-gradient
- background-position
- @keyframes
- transform
- infinite animation

Do not hardcode a one-time animation.

The shimmer must loop continuously while loading.

Recommended animation duration:
approximately 1000–1800ms.

The animation should be linear and smooth.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
4. REUSABLE COMPONENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Create a reusable Skeleton/Shimmer component.

Example:

SkeletonShimmer

or

AnimatedSkeleton

It should support properties such as:

- width
- height
- borderRadius
- margin
- padding
- shape
- optional animation configuration

Examples of shapes:

- Rectangle
- Rounded rectangle
- Circle
- Pill
- Text line

All skeleton elements should use the same reusable shimmer system.

Do not duplicate animation logic throughout the application.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
5. PERFORMANCE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The shimmer must be optimized.

Requirements:

- Avoid creating unnecessary animation controllers.
- Reuse animation logic where possible.
- Avoid excessive widget rebuilds.
- Avoid high CPU/GPU usage.
- Dispose animation resources correctly.
- Stop animation when loading finishes.
- Do not continue animations for removed/off-screen content when unnecessary.
- Maintain smooth rendering.

The loading animation should feel lightweight and polished.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
6. SKELETON COLORS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Use a modern neutral skeleton appearance.

Light theme:

- Soft neutral background
- Light-gray skeleton base
- Slightly brighter shimmer highlight

Dark theme:

- Dark neutral skeleton base
- Slightly lighter shimmer highlight

The colors should integrate with the application's existing theme.

Do not introduce an unrelated color palette.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
7. NO LAYOUT SHIFT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The skeleton must have approximately the same:

- Width
- Height
- Padding
- Margin
- Spacing
- Alignment
- Border radius

as the final content.

When real content appears, the layout should not jump or resize unexpectedly.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
8. LOADING STATES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Handle these states properly:

LOADING:
Show animated skeleton + shimmer.

SUCCESS:
Remove skeleton and show real content.

EMPTY:
Show the application's existing empty state.

ERROR:
Show the application's existing error state/retry UI.

Do not show skeletons after loading has completed.

Do not show a generic CircularProgressIndicator instead of content skeletons unless the existing UI specifically requires one.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
9. RESPONSIVE DESIGN
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The skeleton must work correctly across:

- Mobile
- Tablet
- Desktop
- Web
- Small windows
- Large screens
- Different aspect ratios

Skeleton dimensions should adapt with the real UI.

Do not hardcode desktop-only dimensions.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
10. DIFFERENT SCREEN TYPES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Automatically create skeleton layouts appropriate for the actual screen.

Examples:

SOCIAL FEED:
Avatar + username + text lines + image/media + action buttons.

PROFILE:
Profile avatar + name + bio + statistics + tabs + content cards.

DASHBOARD:
Summary cards + charts + tables + statistics.

E-COMMERCE:
Product image + title + price + rating + buttons.

CHAT:
Avatar + message bubbles + timestamps.

SETTINGS:
Section headings + rows + switches + buttons.

TABLE:
Header + rows + columns + cell placeholders.

Do not force one skeleton layout onto every screen.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
11. ANIMATION CONSISTENCY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

All skeleton elements on the same screen should feel like one coordinated shimmer system.

Avoid:

- Random animation speeds
- Random directions
- Random animation behavior
- Flickering
- Pulsing opacity
- Excessive brightness
- Different animation behavior for every component

The overall effect should feel smooth and unified.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
12. REAL-TIME TRANSITION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

When the data becomes available:

- Stop the shimmer animation.
- Remove the skeleton.
- Display the real content.
- Avoid sudden flashes.
- Avoid blank screens.
- Avoid unnecessary page rebuilds.
- Preserve the current navigation and UI state.

Use a smooth transition only if it does not introduce layout shifting.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
13. EXISTING APPLICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Before implementing the skeleton:

1. Inspect the existing screen/UI.
2. Identify the actual content structure.
3. Create skeletons that match that structure.
4. Reuse existing theme values.
5. Reuse existing responsive layout rules.
6. Follow the existing architecture and coding conventions.
7. Do not modify existing business logic.
8. Do not modify navigation.
9. Do not modify existing functionality.

Only add the loading experience.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
14. IMPORTANT — STATIC SKELETON IS NOT ACCEPTABLE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The implementation is NOT complete if the result looks like:

[ STATIC GRAY BOX ]
[ STATIC GRAY BOX ]
[ STATIC GRAY BOX ]

The implementation MUST look and behave like:

[████░░░░░░░░░░]
[░████░░░░░░░░░]
[░░████░░░░░░░░]
[░░░████░░░░░░░]

where the highlighted section continuously moves across the skeleton.

The shimmer must remain animated for as long as the content is loading.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
15. ACCEPTANCE CRITERIA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Verify the implementation using the following checklist:

✓ Skeleton appears immediately during loading.
✓ Skeleton matches the real UI structure.
✓ Shimmer is visibly moving.
✓ Shimmer moves LEFT → RIGHT.
✓ Shimmer loops continuously.
✓ Every visible skeleton participates in the animation.
✓ Animation is smooth.
✓ Animation is subtle and professional.
✓ No static skeleton remains during loading.
✓ No generic spinner replaces the skeleton.
✓ No blank screen appears.
✓ No layout jumping occurs.
✓ Real content replaces the skeleton after loading.
✓ Loading animation stops after content loads.
✓ Light theme works.
✓ Dark theme works.
✓ Responsive layouts work.
✓ Performance remains smooth.
✓ Existing application functionality remains unchanged.

FINAL REQUIREMENT:

Build a polished, modern Animated Skeleton Loading / Shimmer Loading experience similar in UX quality to modern popular apps and websites.

The shimmer animation itself is mandatory.

Do not implement a static skeleton.

Do not consider the task complete until the shimmer can clearly be seen moving continuously across the loading placeholders.
```

------------------------------------------------------------------------

## Expected Result

The final loading state should:

1.  Immediately show the structure of the real UI.
2.  Display a clearly visible moving shimmer.
3.  Animate continuously from left to right.
4.  Loop smoothly while content is loading.
5.  Avoid layout shifts.
6.  Replace the skeleton with real content when loading finishes.
7.  Work consistently in light and dark themes.
8.  Remain responsive across supported screen sizes.
9.  Avoid unnecessary performance overhead.
10. Never fall back to a static skeleton during normal loading.
