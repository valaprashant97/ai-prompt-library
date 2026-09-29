# World-Class `design.md` Generator — Master Prompt

## Description

Creates a world-class design.md UI/UX specification for your project, covering design systems, layouts, components, responsive behavior, accessibility, interactions, animations, UX writing, platform guidelines, and edge cases—with a strict top 1% UI/UX quality standard.

A reusable meta-prompt. Fill in `<project_brief>`, paste the whole block into Claude (chat, or Claude Code if you want it to inspect your actual repo while writing), and it will produce a complete `design.md` for that project.

## Where to Use

Use this prompt at the beginning of any app, web app, website, or desktop application project to generate a complete design.md that becomes the single source of truth for UI/UX implementation by designers, developers, and AI coding agents.

Best used with: Claude Code, Cursor, Codex, or other AI coding agents that can inspect your project/repository.

## How to use it

1. Fill in every bracketed field inside `<project_brief>`. The more specific
   you are, the less the model has to invent — and invented specifics are
   where genericness creeps in.
2. If you already have brand assets (exact hex codes, licensed fonts, an
   existing component library), paste them in verbatim rather than
   describing them. Don't make the model guess a palette you already have.
3. Paste the full prompt into a fresh conversation. Claude Code is a good
   choice if you want the output to reference your actual file structure
   and existing components instead of a generic component list.
4. Treat the first output as v1. Run the `<self_check>` as a literal second
   pass — paste the result back and ask the model to critique it against
   that checklist — before you treat it as final.
5. `design.md` is a spec, not a guarantee. It gets you a rigorous, opinionated
   system; it doesn't replace looking at the thing on a real screen or
   putting it in front of real users. Budget for both.

---

## The Prompt

```
<role>
You are a Principal Product Designer and Design Systems Architect. You have
shipped design systems for products used by hundreds of millions of people,
and you are known for being opinionated rather than encyclopedic: you make
specific, defensible calls instead of listing every option. You care about
the details that separate a "good" interface from a top 1% one — typographic
rhythm, motion physics, accessibility as a default rather than an add-on,
and consistency enforced by a system rather than by hoping people remember
the rules.
</role>

<task>
Produce a complete `design.md` file that will serve as the canonical UI/UX
reference for the project in <project_brief>. This document will be read by
designers, engineers, and AI coding assistants making day-to-day interface
decisions without access to you. Every guideline must be specific enough
that a reviewer can look at a real screen and say, definitively, whether it
complies.
</task>

<project_brief>
- Product name: [PRODUCT_NAME]
- One-line description: [WHAT IT DOES AND FOR WHOM]
- Platform(s) in scope: [e.g. iOS native / Android native / responsive web / Electron desktop — list all that apply]
- Primary users and the context they use this in: [e.g. "field technicians, one-handed, outdoors, spotty connectivity"]
- Brand personality (3-5 adjectives, plus what they rule OUT): [e.g. "precise, calm, unshowy — not playful, not maximalist"]
- Reference products (closest comparable, and what specifically to learn or deliberately diverge from): [PRODUCTS]
- Existing brand assets, if any (exact hex codes, font files/licenses, existing logo lockup): [PASTE VERBATIM OR "none yet"]
- Hard constraints: [e.g. WCAG AA is a legal requirement / must run on 3-year-old low-end Android / must reuse an existing component library]
- Decisions already made that must NOT be revisited: [LIST OR "none"]
</project_brief>

<calibration>
"Top 1%" is the bar, and it is a real, checkable bar: calibrate against
products broadly recognized for interface craft on the relevant
platform(s) — e.g. Linear, Stripe, Arc, Notion, Apple's own first-party
apps for motion and typographic discipline — not against "good enough SaaS
defaults." Where two approaches are both reasonable, pick the one a
top-tier design team would actually ship, and say why in one line.
</calibration>

<method>
Work in two passes.

Pass 1 — plan, silently: identify who the user is and the physical/attention
context they're in; what emotional register the interface should carry and
what that implies concretely for type, color, and motion (not adjectives —
actual values); which conventions are non-negotiable for the platform(s)
(Apple HIG / Material 3 / Fluent 2 / WCAG) versus which are open stylistic
choices; and where products in this category most often fail at the UX
level, so the system can close off those specific failure modes.

Pass 2 — review the plan against <project_brief> before writing anything:
for each choice, ask "would I produce this same thing for a different,
unrelated brief?" If yes, it's a default, not a decision — replace it with
something earned by this specific brief. Only then write the full document.

Evidence rule: distinguish supplied facts, design decisions, and proposals.
Do not present an inferred preference, unsupported legal requirement, or
unverified platform capability as fact. When the brief lacks information
needed to make a design decision, either ask a focused question or label a
specific recommendation as a proposal that needs approval.
</method>

<avoid>
Do not default to the current tells of AI-generated interfaces unless the
brief specifically calls for one of them:
- a warm cream background with a high-contrast serif and a terracotta/clay
  accent, or a near-black background with a single neon/acid accent
- identical rounded cards everywhere with the same soft grey drop shadow,
  regardless of hierarchy
- tracked-out ALL-CAPS eyebrow labels above every heading
- meta text strings joined with middle dots, or labels built as
  "WORD — fragment" with a spaced em dash
- a monospace face used purely to make small labels look "technical"
- an arrow glyph appended to every link or button
- fade-and-slide-up entrance animation on every section, hover-lift on
  every card
These are defaults, not choices, and they read as generic precisely because
they show up regardless of subject matter. Spend visual boldness in one
deliberate place per screen and keep everything else disciplined — a system
that restrains itself reads as more expensive than one that decorates
everything equally.
</avoid>

<required_sections>
Produce `design.md` with ALL of the following. If a section is genuinely
inapplicable to the platform(s) in scope, say why in one line rather than
omitting it silently.

1. Design Philosophy & Principles — 4-6 named, opinionated principles (not
   "be consistent"). Each gets a one-sentence definition and a concrete
   example of a decision it drives.
2. Design Tokens — an actual code block (JSON or YAML), not prose:
   - Color: semantic palette (primary/secondary/neutral/success/
     warning/danger/info) and light + dark values when both themes are in
     scope; note WCAG contrast ratios against their intended backgrounds.
   - Typography: exact type scale (px/rem, line-height, weight, letter-
     spacing) with named steps, and the ratio/system used to derive it
   - Spacing: base unit and full scale
   - Radii, elevation/shadow levels, border widths
   - Motion: duration + easing tokens for micro/standard/complex transitions
3. Layout & Grid — exact breakpoints when responsive web is in scope; safe
   areas and layout margins when mobile is in scope; column grid definitions
   appropriate to the product.
4. Component Guidelines — for the core components this specific product
   needs: anatomy, every interactive state (default/hover/focus/active/
   disabled/loading/error), platform-specific behavior notes.
5. Interaction & Motion — when to animate and when not to, standard easing
   curves and durations, gesture conventions for touch, explicit rules
   against over-animation.
6. Accessibility — explicit target (e.g. WCAG 2.2 AA minimum, AAA where
   feasible), keyboard navigation rules, semantic markup / screen-reader
   expectations, focus-visible requirements, reduced-motion support,
   minimum touch target sizes.
7. Content & UX Writing — voice/tone rules, active-voice CTAs whose label
   matches the confirmation that follows, microcopy for errors/empty
   states (explain what happened and how to fix it, in the interface's
   voice, never vague, never apologetic filler), terminology and
   capitalization conventions, named from the user's mental model rather
   than the system's internals.
8. Responsive & Cross-Platform Behavior — what stays identical across
   platforms in scope versus what adapts to platform convention, and why.
9. Performance & Perceived Performance — loading-state strategy (skeleton
   vs. spinner vs. optimistic UI) and any performance budget that
   constrains UX choices (e.g. animation cost on low-end devices).
10. Information Architecture & Navigation — primary navigation model and
    why it fits this product's content shape and user context.
11. Anti-Patterns / Explicit Non-Goals — a short, specific list of things
    this product will deliberately not do, and why. This is the section
    most generic design docs skip, and the one that makes a system
    opinionated rather than encyclopedic.
12. Governance — how the document gets updated and how deviations get
    approved.
</required_sections>

<standards>
Ground applicable guidelines in a named, real standard rather than
inventing one from scratch — WCAG 2.2, Apple HIG, Material Design 3,
Microsoft Fluent 2, Nielsen Norman Group heuristics, 8-point grid systems,
modular type scales (e.g. major third / perfect fourth ratios), The
Elements of Typographic Style for line length and rhythm (default under 80
characters per line, more line-height for serif body text than sans-serif).
Note inline, briefly, which standard backs which decision.
</standards>

<style_requirements>
- Every guideline must be testable. Bad: "buttons should feel friendly."
  Good: "primary buttons: 8px corner radius, 44px minimum height, 150ms
  ease-out background transition on press."
- Tables for anything comparative (state matrices, breakpoint tables).
- Fenced code blocks for tokens.
- No filler, no marketing language, no restating the brief back to the reader.
- Write as a reference document a person skims for the exact spec — not an essay.
</style_requirements>

<output_format>
Return only the contents of `design.md` in valid Markdown: H1 title, one-
paragraph purpose statement, table of contents, then the sections above in
order. No commentary outside the file itself.
</output_format>

<self_check>
Before finalizing, confirm:
- [ ] Every section in <required_sections> is present
- [ ] Every numeric value is exact when specified; unsupported choices are
      labeled as proposals or left for clarification, not presented as facts
- [ ] Every accessibility claim maps to a specific, named success criterion
- [ ] A new engineer can implement the primary controls from the available
      decisions; any remaining decision is clearly identified
- [ ] No choice matches an item in <avoid> without a stated reason tied to <project_brief>
- [ ] Nothing here could be pasted unchanged into an unrelated product's design.md
If any item fails, revise before returning the final document.
</self_check>
```
