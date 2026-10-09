# Light & Dark Mode Implementation Prompt

> **Description:** A reusable prompt for adding Light Mode, Dark Mode, and optional System Mode to an existing application without changing its existing UI design, functionality, navigation, or user experience.

## Where to Use This Prompt

Use this prompt when:
- An existing project needs Light and Dark Mode support.
- You want to convert hardcoded theme colors into a centralized theme system.
- You want theme preferences to persist after restarting the app.
- You want both themes to remain visually consistent and accessible.
- You want an AI coding assistant to implement the theme without redesigning the application.

### Recommended Usage

Give this prompt to your AI coding assistant **before asking it to implement or refactor the project's theme system**.

It can be used with existing projects in tools such as:
- Claude
- Cursor
- Windsurf
- GitHub Copilot
- Other AI coding assistants

**Important:** This prompt is intended for an existing project. The AI should first analyze the current codebase and then add the theme system while preserving existing functionality and UI.

```text
Add a complete, production-ready Light Mode and Dark Mode system to the existing project.

IMPORTANT:
The existing application is already working. Add theme support without changing
the existing functionality, navigation, user flow, or overall UI design.

## Requirements

- First analyze the existing project and understand its current UI, colors,
  typography, components, screens, navigation, and theme-related code.
- Add both Light Mode and Dark Mode.
- Keep the existing UI design and visual identity unchanged as much as possible.
- Do not redesign screens just because dark mode is being added.
- Replace hardcoded theme-dependent colors with centralized theme values.
- Use a centralized theme system instead of defining colors individually throughout the project.
- Keep colors, typography, spacing, shapes, buttons, cards, dialogs, inputs,
  navigation, and other components consistent between themes.
- Ensure text remains readable and accessible in both themes.
- Ensure icons, borders, dividers, cards, backgrounds, and other UI elements
  have appropriate colors in both themes.
- Avoid hardcoded colors that cannot adapt to the selected theme.
- Reuse existing components and styles wherever possible.
- Do not duplicate entire screens for Light and Dark Mode.
- Use the same UI components with theme-aware styling.

## Theme Selection

Support:

- Light Mode
- Dark Mode
- System / Automatic Mode, if supported by the platform

If a theme selector already exists, integrate with it instead of creating
another one.

If no theme selector exists, add a simple option in the existing settings area
when theme choice fits the product. Do not create a new settings screen solely
to expose this control; if there is no suitable place, follow the project's
existing preferences pattern.

## Theme Persistence

- Remember the user's selected theme.
- Restore the selected theme when the application is reopened.
- If System / Automatic Mode is supported, follow the device's system theme.
- Changing the theme should update the application without requiring unnecessary
  navigation or restarting the app.

## UI Consistency

Ensure the following adapt correctly to both themes:

- App background
- Surface/background colors
- Cards
- Text
- Headings
- Secondary text
- Buttons
- Input fields
- Borders
- Dividers
- Icons
- Navigation
- Dialogs
- Bottom sheets
- App bars
- Lists
- Switches
- Checkboxes
- Radio buttons
- Progress indicators
- Charts
- Images where applicable
- Empty states
- Loading states
- Error states
- Success states

## Accessibility

- Maintain sufficient contrast in both themes.
- Do not rely only on color to communicate important information.
- Ensure disabled, selected, focused, and active states remain distinguishable.
- Keep text readable across different brightness levels.

## Existing Code Quality

- Follow the existing project architecture.
- Follow clean coding principles.
- Keep theme-related code centralized and reusable.
- Avoid duplicate theme logic.
- Avoid unnecessary dependencies.
- Do not create unnecessary files or abstractions.
- Keep responsibilities separated properly.
- Use meaningful names.
- Add comments only where they provide useful context.

## Important Restrictions

DO NOT:

- Redesign the application.
- Change existing functionality.
- Change navigation.
- Change business logic.
- Remove existing features.
- Replace existing components unnecessarily.
- Create duplicate screens for Light and Dark Mode.
- Hardcode theme colors throughout individual screens.
- Introduce unnecessary packages or dependencies.
- Change the existing UI layout unless required for theme compatibility.

## Refactoring Existing Colors

If the existing project contains hardcoded colors:

1. Identify theme-dependent colors.
2. Move them into the centralized theme system.
3. Replace their direct usage with theme-aware values.
4. Preserve the existing Light Mode appearance as closely as possible.
5. Create appropriate Dark Mode equivalents.

Do not blindly replace every color. Preserve colors that are intentionally
independent of the theme, such as brand colors, status colors, or illustrations,
when appropriate.

## Testing

After implementation, verify:

- Light Mode works correctly.
- Dark Mode works correctly.
- System Mode works correctly if implemented.
- Theme selection persists after restarting the app.
- Every screen supports both themes.
- No text becomes invisible or difficult to read.
- No icons disappear.
- No cards, dialogs, inputs, or navigation elements remain incorrectly colored.
- No layout or functionality is broken.
- No hardcoded theme-dependent colors remain unnecessarily.
- Existing functionality behaves exactly as before.

## Final Goal

Add a complete Light/Dark/System theme system while preserving the existing
application's functionality, design, navigation, and user experience.

The result should feel like the same application with a professionally
implemented theme system — not a redesigned application.

PRINCIPLE:

"Add the theme, don't redesign the product."

```