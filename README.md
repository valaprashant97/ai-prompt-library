# AI Prompt Library

Reusable prompts and engineering guidelines for software architecture,
requirements discovery, code quality, and UI/UX work.

## Start here

1. Choose a prompt from the catalog below.
2. Open the linked document and copy the prompt block or guidelines.
3. Replace project-specific placeholders and add the context the AI needs.
4. Review the output against the document's checklist before using it.

## Prompt catalog

| Area | Use this when you need to... | Document |
| --- | --- | --- |
| Architecture | Define a clean, scalable project structure | [Project architecture and file/folder structure](Architecture%20%26%20FileFolder%20Structure/Project%20Architecture%20%26%20FileFolder%20Structure%20Guidelines%20.md) |
| Engineering | Set project-wide coding and development standards | [Coding instructions and development principles](Coding%20Instructions%20%26%20Development%20Principles/Coding%20Instructions%20%26%20Development%20Principles.md) |
| Documentation | Decide when and how to write useful comments | [Code commenting and documentation](Code%20Commenting%20%26%20Documentation/Code%20Commenting%20%26%20Documentation%20Guidelines.md) |
| Requirements | Turn product context into customer-focused requirements | [Customer-based requirements gathering](Requirements%20Gathering%20From%20Ai/customer-based-requirements-gathering-prompt.md) |
| UI/UX | Establish general UI quality and accessibility rules | [UI/UX design and quality](UI%20%26%20UX/UI%26UX%20Design%20%26%20Quality%20Guidelines.md) |
| UI/UX | Make an existing interface adapt across screen sizes | [Responsive UI system prompt](UI%20%26%20UX/responsive-ui-prompt.md) |
| UI/UX | Apply concise responsive design rules | [Responsive design guidelines](UI%20%26%20UX/Responsive%20Design%20Guidelines.md) |
| UI/UX | Add light, dark, or system theme support | [Light and dark mode implementation](UI%20%26%20UX/light-dark-mode-prompt.md) |
| UI/UX | Generate a complete, opinionated design specification | [UI/UX design master prompt](UI%20%26%20UX/ui-ux-design-master-prompt.md) |

## Which UI/UX prompt should I use?

- Use **UI/UX design and quality** for baseline standards that apply to every
  interface.
- Use **Responsive UI system prompt** when an AI assistant should inspect and
  update an existing project for responsive behavior.
- Use **Responsive design guidelines** as a short checklist or standalone
  reference.
- Use **Light and dark mode implementation** when adding theme support without
  redesigning the product.
- Use **UI/UX design master prompt** at the start of a project when a detailed
  `design.md` specification is needed.

These prompts are complementary: combine a baseline guideline with one
task-specific implementation prompt instead of pasting every UI/UX document
into the same request.

## Suggested workflow

### Before implementation

- Run the requirements prompt with the available product and project context.
- Resolve questions marked **Needs Clarification**.
- Use the architecture and engineering guidelines as project constraints.
- Use the master prompt only when a formal design specification is required.

### During implementation

- Give the AI the relevant task-specific prompt and the current project
  context.
- Preserve existing behavior unless the request explicitly changes it.
- Apply the commenting guidelines when adding documentation.
- Use the responsive or theme prompts only for the surfaces they address.

### Before merging

- Check relevant loading, empty, success, and error states.
- Check accessibility, responsive behavior, and theme behavior when applicable.
- Replace unresolved placeholders, remove temporary debugging output, and
  update or remove stale TODOs.
- Update the relevant prompt when a newly discovered rule should be reusable.

## Repository conventions

- Keep prompts grouped by subject area.
- Prefer descriptive, stable filenames.
- Keep reusable instructions framework-agnostic unless a platform is part of
  the requirement.
- State assumptions and mark unresolved decisions as **Needs Clarification**.
- Avoid adding duplicate prompts; extend an existing document when the scope
  is the same.
- Keep prompt output formats explicit so results can be reviewed consistently.
- Treat each document as standalone; link related guidance instead of assuming
  an AI tool can access another file automatically.

## Contributing a prompt

1. Add the document to the closest existing subject folder.
2. Start with a clear title and a short description of when to use it.
3. Define the expected role, task, constraints, and output format.
4. Include edge cases and a verification checklist where relevant.
5. Add the document to the catalog above.
6. Check every link from the README before submitting the change.

## Maintenance

Prompts should be reviewed when model capabilities, platform guidance, or
project workflows change. Keep the library focused on reusable guidance rather
than one-off project decisions.
