# Coding Instructions & Development Principles

```text
Build this project using clean, scalable, maintainable, and production-quality code.

## 1. Code Quality

* Write clean, readable, and well-structured code.
* Follow the official best practices of the chosen programming language/framework.
* Use meaningful names for variables, functions, classes, files, and folders.
* Avoid unnecessary complexity.
* Prefer simple and maintainable solutions over clever solutions.
* Do not write duplicate code.

## 2. Architecture

* Follow a clear and scalable project architecture.
* Separate UI, business logic, data handling, and external services.
* Keep screens, widgets, and components focused on presentation.
* Keep business logic outside the UI layer.
* Use reusable components wherever possible.
* Keep dependencies between modules low.

## 3. DRY Principle

* Do not repeat the same code in multiple places.
* Create reusable functions, components, utilities, or services when appropriate.
* Avoid copy-pasting similar logic.

## 4. SOLID Principles

Follow SOLID principles wherever applicable:

* Single Responsibility Principle
* Open/Closed Principle
* Liskov Substitution Principle
* Interface Segregation Principle
* Dependency Inversion Principle

Do not over-engineer the project just to follow SOLID.

## 5. KISS Principle

* Keep implementations simple.
* Avoid unnecessary abstractions.
* Do not create extra classes or files unless they provide a clear benefit.
* Prefer straightforward solutions.

## 6. YAGNI Principle

* Implement only the features currently required.
* Do not add speculative features.
* Do not add unnecessary libraries or dependencies.

## 7. Reusability

* Create reusable UI components for repeated elements.
* Create reusable services and utilities for common operations.
* Avoid creating multiple slightly different implementations of the same functionality.

## 8. State Management

* Keep application state predictable.
* Separate state management from UI rendering.
* Avoid unnecessary rebuilds or re-renders.
* Update only the required part of the UI when possible.

## 9. Error Handling

* Handle errors properly.
* Handle null values, invalid input, API failures, database failures, permissions, and unexpected states.
* Never silently ignore important errors.
* Show meaningful error messages to users.
* Prevent avoidable application crashes.

## 10. Performance

* Avoid unnecessary API calls.
* Avoid unnecessary database queries.
* Avoid unnecessary UI rebuilds.
* Use caching where appropriate.
* Optimize expensive operations.
* Do not sacrifice readability for minor performance improvements unless necessary.

## 11. Security

* Never hardcode passwords, API keys, tokens, or secrets.
* Validate user input.
* Follow secure storage practices.
* Do not expose sensitive information in logs.
* Use proper authentication and authorization mechanisms where required.

## 12. Database & API

* Keep database and API logic separate from UI code.
* Use proper models and data classes.
* Handle loading, success, empty, and error states.
* Validate API responses before using them.
* Handle network failures gracefully.

## 13. UI/UX Design & Quality Guidelines

* Create a clean, modern, and professional UI.
* Keep the UX simple, intuitive, and user-friendly.
* Maintain consistent design across all screens.
* Use proper spacing, padding, alignment, and visual hierarchy.
* Use clear, readable, and well-balanced typography.
* Use a consistent color palette, icon style, and component design.
* Make the UI responsive and adaptive for different screen sizes.
* Keep navigation simple, predictable, and easy to understand.
* Minimize unnecessary steps, clicks, and user interactions.
* Provide clear loading, empty, success, and error states.
* Use smooth and subtle animations and transitions where appropriate.
* Make buttons and interactive elements easy to identify and use.
* Ensure sufficient touch target sizes for mobile devices.
* Provide immediate visual feedback after user actions.
* Avoid unnecessary decoration, clutter, and excessive information.
* Prioritize usability and accessibility over visual complexity.
* Follow platform-specific design guidelines and conventions.
* Ensure every screen has a clear purpose and user flow.
* Handle edge cases gracefully without breaking the UI.
* Confirm destructive actions when they are consequential or difficult to
  reverse; do not add needless confirmation steps for easily reversible
  actions.
* Make important actions visually clear and easy to access.
* Keep forms simple, organized, and easy to complete.
* Show meaningful validation messages for incorrect input.
* Avoid excessive animations that can distract the user.
* Optimize UI performance and avoid unnecessary rebuilds.

### Overall UI/UX Goal

Build a modern, clean, intuitive, responsive, accessible, visually consistent, and production-ready UI/UX that provides a smooth and enjoyable user experience.

## 14. Project Architecture & File/Folder Structure Guidelines

* Use a clean, scalable, and logical project structure.
* Organize files by feature or responsibility.
* Keep related files together.
* Separate UI, business logic, data, services, models, and utilities.
* Keep each file focused on a single responsibility.
* Avoid unnecessarily large files.
* Avoid deeply nested folders unless necessary.
* Use consistent and meaningful file and folder names.
* Follow the naming conventions of the selected framework.
* Create reusable components in appropriate shared or common folders.
* Keep API and database logic separate from UI code.
* Keep models and data classes separate from business logic.
* Avoid duplicate files or duplicate implementations.
* Do not create unnecessary folders or files.
* Reuse existing files and components whenever possible.
* Before creating a new file, check whether an existing file can be reused.
* Keep the structure easy for another developer to understand and maintain.
* Do not reorganize the entire project unnecessarily when adding a feature.
* When adding a new feature, place its files in the appropriate feature or module folder.
* Keep configuration and environment-related files separate from application logic.
* Maintain a consistent structure throughout the entire project.

### Overall Project Structure Goal

Maintain a clean, predictable, scalable, and maintainable project structure that makes the codebase easy to navigate, understand, test, and extend.

## 15. Code Commenting & Documentation Guidelines

* Write clear, concise, and meaningful comments.
* Add comments only when they provide useful context.
* Do not comment obvious or self-explanatory code.
* Explain why something is done, not just what the code does.
* Add comments for complex business logic or non-obvious implementations.
* Document important algorithms and calculations when necessary.
* Add comments for important edge cases and special conditions.
* Explain workarounds when they are required due to framework or platform limitations.
* Keep comments up to date whenever the related code changes.
* Avoid outdated or misleading comments.
* Do not use comments to compensate for unclear code; prefer meaningful names and clean code.
* Keep comments short and easy to understand.
* Use consistent comment formatting throughout the project.
* Add documentation for public classes, methods, APIs, or reusable components when appropriate.
* Do not add excessive comments that make the code harder to read.
* Never leave unnecessary TODO, FIXME, or debug comments in production code.
* Remove temporary debugging comments before completing the implementation.

### Overall Commenting Goal

Use comments to make complex or non-obvious code easier to understand without creating unnecessary noise or duplicating what the code already explains.

## 16. Dependencies

* Do not add a package or library unless it is actually needed.
* Prefer built-in functionality when it is sufficient.
* Before adding a dependency, consider whether the same functionality can be implemented cleanly without it.

## 17. Debugging

When fixing a bug:

1. Identify the root cause.
2. Fix the root cause instead of hiding the symptom.
3. Check related functionality for regressions.
4. Keep the fix minimal and maintainable.
5. Do not rewrite unrelated code.

## 18. Existing Code

* Before changing code, understand the existing architecture and implementation.
* Reuse existing utilities and components when possible.
* Do not unnecessarily rewrite working code.
* Preserve existing functionality unless the requirement explicitly asks for a change.

## 19. Development Process

Before implementing a major feature:

1. Understand the requirement.
2. Inspect the existing project structure.
3. Identify affected files.
4. Plan the implementation.
5. Implement incrementally.
6. Check for errors.
7. Verify that existing features still work.

## 20. Important Rule

Do not generate code just to make the feature appear complete.

The implementation must be:

* Correct
* Maintainable
* Scalable
* Readable
* Performant
* Secure
* Consistent with the existing project architecture

If an existing implementation is already good, improve it instead of unnecessarily replacing it.

### Priority

Correctness → Maintainability → Readability → Performance → Simplicity
```