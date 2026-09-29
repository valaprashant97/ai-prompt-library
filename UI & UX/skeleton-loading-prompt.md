# Skeleton Shimmer Loading UI Prompt

## When to Use

Use this prompt when an app or website needs to load content from an API, database, Firebase, server, local storage, or any other data source.

It is especially useful when:

- The screen takes time to load data.
- You want to avoid showing a blank screen.
- You want to replace a basic `Loading...` text or spinner.
- You are loading cards, lists, tables, dashboards, profiles, or feeds.
- You want a professional and modern loading experience.
- You need responsive loading UI for mobile, tablet, desktop, and web.
- You want to prevent layout shifting while content is loading.

---

## Description

This prompt creates a **Skeleton Loading / Shimmer Loading UI** based on the provided reference image.

Instead of displaying a blank screen or a simple loading spinner, the application displays placeholder elements that represent the structure of the actual content.

The skeleton placeholders use a light-gray/neutral appearance with a smooth shimmer animation moving across them.

When the actual data finishes loading, the skeleton automatically disappears and is replaced by the real content.

### Key Features

- Professional Skeleton Loading UI
- Smooth left-to-right shimmer animation
- Content-shaped placeholders
- Responsive design
- Reusable skeleton components
- Supports cards, lists, tables, images, buttons, and text
- Prevents layout shifting
- Automatically switches to real content
- Consistent loading experience throughout the application
- Works across mobile, tablet, desktop, and web

---

## Prompt

```text
Implement a professional Skeleton Loading / Shimmer Loading UI throughout the app/website.

Use the uploaded reference image as the visual reference for the loading state. Before the actual content is available, display skeleton placeholders that match the structure, size, spacing, alignment, border radius, and layout of the real content.

Requirements:

- Use light-gray skeleton placeholders on a soft neutral background.
- Add a smooth left-to-right shimmer animation across all skeleton elements.
- Match the actual content layout instead of using generic loading spinners.
- Create placeholders for text lines, cards, images, buttons, tables, lists, and other UI components where required.
- Preserve the exact dimensions and spacing of the final UI to prevent layout shifting.
- Show skeletons only while data/content is loading.
- Automatically replace skeletons with the real content when loading completes.
- Keep the shimmer animation smooth, subtle, and professional.
- Make the skeleton UI fully responsive for mobile, tablet, desktop, and web.
- Create reusable Skeleton/Shimmer components so the implementation remains consistent throughout the project.
- Support different skeleton layouts based on the actual screen content.
- Avoid excessive animation or distracting visual effects.
- Do not change the existing app's design, functionality, navigation, or content.
- Do not replace the skeleton with a generic circular progress indicator unless specifically required.
- Ensure there are no sudden flashes, jumps, or layout changes during loading.
- Handle loading, success, empty, and error states cleanly.
- Keep the implementation optimized and avoid unnecessary rebuilds or performance issues.
- Follow the existing project's architecture, coding style, theme system, and responsive design rules.
- Reuse existing components and styles wherever possible instead of creating duplicate implementations.

The final result should provide a polished, modern, production-ready Skeleton Shimmer Loading experience that closely follows the uploaded reference image while adapting naturally to the existing application's UI.
```