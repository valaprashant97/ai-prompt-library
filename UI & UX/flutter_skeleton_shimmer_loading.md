# Skeleton Shimmer Loading Prompt

## When to Use

Use this prompt when you want to add a professional, reusable **Skeleton
Shimmer Loading System** to a Flutter project.

It is especially useful when: - Screens load data asynchronously. - You
want Instagram-style animated skeleton placeholders. - You need
consistent loading states across multiple screens. - You want to prevent
layout shifts while content is loading. - The project supports multiple
Flutter platforms.

## Short Description

This prompt instructs an AI coding tool to implement a reusable Skeleton
Shimmer Loading system using the `shimmer` package while preserving the
existing UI, architecture, business logic, and functionality.

## Prompt

```text
Implement a professional, reusable **Skeleton Shimmer Loading System**
throughout this Flutter project using the `shimmer` package.

-   Add the latest stable `shimmer` dependency.
-   Create reusable shimmer widgets/components.
-   Apply skeleton loading to all appropriate screens and asynchronous
    content.
-   Match skeleton layouts with the actual UI structure, dimensions,
    spacing, and typography.
-   Use smooth left-to-right shimmer animation.
-   Support Light Mode and Dark Mode using the existing theme.
-   Show skeleton while content is loading, then seamlessly replace it
    with the actual UI.
-   Handle loading, success, empty, and error states separately.
-   Prevent layout shifts, flickering, and unnecessary rebuilds.
-   Keep the implementation lightweight and performant.
-   Follow the existing project architecture and state-management
    pattern.
-   Do not change existing UI design, navigation, business logic,
    database logic, API logic, or functionality.
-   Do not duplicate shimmer code; centralize reusable components.
-   Ensure the implementation works correctly on all platforms supported
    by the Flutter project.
-   Run `flutter analyze` and fix all issues introduced by the
    implementation.
```
