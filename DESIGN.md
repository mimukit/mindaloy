---
version: alpha
name: Mindaloy
description: Approved concept 05 with charcoal cards and flat neutral controls in light and dark modes.
omitted:
  - section: spacing
    reason: No application CSS or approved numeric spacing scale exists.
  - section: rounded
    reason: The approved images show rounded shapes but do not establish a measured radius scale.
colors:
  primary: "#3A3A3A"
  on-primary: "#ECECE6"
  surface-dark: "#1A1A1A"
  sidebar-dark: "#202020"
  card-dark: "#303030"
  on-surface-dark: "#EAEAE5"
  muted-dark: "#A8A8A2"
  surface-light: "#DEDEDC"
  sidebar-light: "#D2D2D0"
  on-surface-light: "#30302E"
  muted-light: "#62625E"
  card-backing: "#333333"
  card-metadata: "#C0C0BA"
  edge-dark: "#414141"
  control-edge: "#666666"
  marker-dark: "#B6B6B0"
  marker-light: "#4A4A48"
typography:
  headline:
    fontFamily: Newsreader
  body:
    fontFamily: DM Sans
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body}"
  grade-control:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body}"
  navigation-selected:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body}"
  page-dark:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.on-surface-dark}"
    typography: "{typography.body}"
  heading-dark:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.on-surface-dark}"
    typography: "{typography.headline}"
  sidebar-dark:
    backgroundColor: "{colors.sidebar-dark}"
    textColor: "{colors.on-surface-dark}"
  card-dark:
    backgroundColor: "{colors.card-dark}"
    textColor: "{colors.on-surface-dark}"
  metadata-dark:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.muted-dark}"
  page-light:
    backgroundColor: "{colors.surface-light}"
    textColor: "{colors.on-surface-light}"
    typography: "{typography.body}"
  heading-light:
    backgroundColor: "{colors.surface-light}"
    textColor: "{colors.on-surface-light}"
    typography: "{typography.headline}"
  sidebar-light:
    backgroundColor: "{colors.sidebar-light}"
    textColor: "{colors.on-surface-light}"
  card-light:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  metadata-light:
    backgroundColor: "{colors.surface-light}"
    textColor: "{colors.muted-light}"
  card-metadata:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.card-metadata}"
  card-backing:
    backgroundColor: "{colors.card-backing}"
  separator-dark:
    backgroundColor: "{colors.edge-dark}"
  control-edge:
    backgroundColor: "{colors.control-edge}"
  selection-marker-dark:
    backgroundColor: "{colors.marker-dark}"
  selection-marker-light:
    backgroundColor: "{colors.marker-light}"
---

# Mindaloy design system

## Overview

Mindaloy uses neutral backgrounds, charcoal collection cards, and flat controls. Serif headings distinguish learning content from navigation and supporting text. Card stacks provide restrained depth.

The owner approves the final concept 05 mockups on 2026-10-22. The references cover desktop collections and a phone review after reveal.

| Mode | Approved reference | Generation prompt |
|------|--------------------|-------------------|
| Dark | [Final dark mockup](output/design/mindaloy-dark-concept-05-flat-controls.png) | [Edit prompt](output/design/mindaloy-dark-concept-05-flat-controls-prompt.txt) |
| Light | [Final light mockup](output/design/mindaloy-light-concept-05-flat-controls.png) | [Edit prompt](output/design/mindaloy-light-concept-05-flat-controls-prompt.txt) |

[Issue #2](https://github.com/mimukit/mindaloy/issues/2) preserves GitHub attachment copies of the [dark reference](https://github.com/user-attachments/assets/b3295cf5-9b40-4125-88fd-ae627547bbcb) and [light reference](https://github.com/user-attachments/assets/cc970a93-44c4-435b-a18b-1f94014c7594).

This system is proposed from supplied, approved mockups and briefs, not extracted from application code. The repository has no application UI or token home. All YAML tokens have the supplied classification. No values are consolidated.

The mockup prompts supply the numeric colors. Generated pixels can differ from those values. The tokens define implementation colors; the approved images define composition and visual hierarchy.

Integration settings have no approved image. The keyboard rules and request states below provide implementation guidance from the visual plan. They are not evidence of a tested interface. Keep issue #2 open until its remaining reference requirements are satisfied.

## Colors

Use charcoal as the default primary color in both modes. Primary actions have light labels. Theme-specific neutral markers show selection and review progress.

| Role | Dark mode | Light mode |
|------|-----------|------------|
| Page | `surface-dark` | `surface-light` |
| Sidebar and top bar | `sidebar-dark` | `sidebar-light` |
| Main text outside cards | `on-surface-dark` | `on-surface-light` |
| Secondary text outside cards | `muted-dark` | `muted-light` |
| Collection and key-points cards | `card-dark` | `primary` |
| Text on cards | `on-surface-dark` | `on-primary` |
| Primary and grade controls | `primary` with `on-primary` | `primary` with `on-primary` |
| Selection and completed progress | `marker-dark` | `marker-light` |

Use `card-backing` for the offset layers behind collection cards. Use `card-metadata` for secondary text on the light mode's charcoal cards. Use `edge-dark` for quiet dark separators.

A primary button can use one uniform `control-edge` stroke. Do not add a second border or reflective edge. Keep navigation and progress markers neutral.

Do not restore lime, blue, violet, or teal accents from earlier concepts. User-selectable primary colors remain future work.

Error, warning, hover, and active colors have no approved numeric values. Do not create tokens for them from guesses. Use text and control state to communicate meaning until those values are selected.

## Typography

Use Newsreader for the wordmark, collection headings, collection names, and review cue. Use DM Sans for navigation, counts, body text, labels, and buttons.

The owner selects option 2, Newsreader with DM Sans, on 2026-10-22. The [font comparison](output/design/mindaloy-font-comparison.html) records the alternatives. This selection replaces the unspecified fonts in the earlier mockups. Preserve their layout and colors.

Use `"Newsreader", serif` and `"DM Sans", sans-serif` as the CSS font stacks. Production font files, sizes, weights, line heights, and letter spacing remain unspecified. The comparison contains subset font files for sample text, with [license files](output/design/font-licenses/).

Make the cue the most prominent review text. Keep key points and typed answers readable without magnification. Do not use low-contrast small text to reproduce incidental image shading.

## Layout

Desktop collections use a left sidebar and a main content area. The sidebar contains the collection list, a review entry, and integration settings. The main area has a quiet top bar, heading, due summary, collection cards, and one review action.

Show the three sample collections as one row when space permits. Reduce the column count as available space decreases. Keep collection names and due counts together. Do not force horizontal scrolling.

The phone review uses one content column. Its order is collection context, progress, cue, typed answer, revealed key points, and grade controls. The supplied board places this phone reference beside desktop collections for comparison. That board arrangement is not an application layout.

The sidebar must not consume review space on a phone. Provide a clear return control. Keep the current collection and progress visible during review.

Before reveal, replace the read-only typed answer with a labeled multiline input. Hide key points and grades. Keep the reveal action reachable when the software keyboard is open. Let the page scroll instead of covering the input or action.

After reveal, show the submitted answer and key points together. The approved phone reference has four grade segments in one row. If labels or targets no longer fit, wrap them into two rows without changing their reading order.

Use targets of at least 44 by 44 CSS pixels, as recorded in the visual plan. This is an interaction requirement, not an extracted spacing token. Numeric gutters, breakpoints, sidebar width, and the spacing scale remain unspecified.

## Elevation & Depth

Collection cards and the key-points card retain subtle depth. Use a small number of offset backing layers and short soft shadows. Avoid large floating shadows or colored atmospheric light.

Buttons are flat in both modes. Primary actions, grade segments, and selected navigation have no gradients, bevels, reflective highlights, inset shadows, or drop shadows. A single uniform border can separate a control from its background.

Do not apply the card's material to a button. Any residual shading in generated control pixels does not authorize a raised button.

Exact shadow dimensions are unspecified. The schema has no elevation token group. Keep this distinction in prose until implementation establishes measured values.

## Shapes

Collection cards and the key-points card have rounded corners. The review action and grade control have pill shapes. App corners in the mockup frame illustrate the reference presentation, not a browser-window requirement.

Preserve the card stack's small offsets. Keep icons simple and use a consistent outline style. Do not treat decorative backing layers as separate interactive targets.

No numeric radius scale is established. The YAML deliberately omits `rounded` rather than treating generated image dimensions as measurements.

## Components

### Collections

Show a collection name, total card count, and due count. The review action names its scope. The sample action reviews all 24 due cards; it does not review only the selected collection's 12 cards.

Treat the mockup counts as sample data. Derive real counts from the API. Do not introduce learned scores, streaks, or charts from rejected concepts.

### Primary actions and navigation

Use `button-primary` for the main review action. Keep secondary actions visually quieter. Use a flat selected navigation fill and a neutral marker.

Hover and pressed states must remain flat. Provide a visible keyboard focus indicator. Do not hide focus to preserve the mockup's appearance. Exact state colors and focus geometry require implementation review.

### Review

Start with the cue and a labeled answer input. Reveal key points only after the learner requests them. Preserve the typed answer for comparison.

Show the four grades after reveal in this order: Again, Hard, Good, Easy. Every segment starts neutral and unselected. The learner selects the grade; Mindaloy does not assess the answer with AI.

The visual plan proposes these keyboard rules.

| Key | Behavior |
|-----|----------|
| Enter in the input | Add a new line. |
| Ctrl+Enter or Cmd+Enter in the input | Reveal key points. |
| 1, 2, 3, 4 after reveal | Select Again, Hard, Good, Easy respectively. |
| Tab and Shift+Tab | Move through visible controls in content order. |

Ignore grade shortcuts while the learner edits text. Move focus to the grade group after reveal. After a confirmed save, move focus to the next answer input.

Disable duplicate grade submission while a save is pending. Advance only after server confirmation. Keep the same client event ID when a request needs retry.

### Integration settings

Apply the same page colors, type roles, and flat controls. This screen still needs an approved visual reference.

Document the key name, permitted collections, permitted operations, and last use. Provide key creation and revocation. Show a new key value once with a copy control and an instruction to save it.

Make collection scope and operation scope visible before creation. Do not imply that a key can manage other keys. Confirm revocation before it removes access.

### Loading, empty, and error states

| State | Required behavior |
|-------|-------------------|
| Collections loading | Show a text loading status. Keep the page structure stable. Do not show fabricated counts. |
| No collections | Explain that no collections exist. Provide a create action. |
| No due cards | State that no cards are due. Keep collection management available. |
| Review loading | Keep the current review visible until the next card is ready. Disable submission while needed. |
| Review save pending | Show a saving status. Prevent duplicate submission. Preserve the answer. |
| Request failure | Name the failed action and provide retry. Do not discard the answer or selected grade. |
| Session expired | Explain that sign-in is required. Preserve the current answer while access is restored where possible. |
| Connection lost | Explain that the save is unconfirmed. Keep the current card and provide retry after reconnection. |

Full offline reviews, pending-review queues, and sync dashboards are outside the first release's approved issue #1 scope. Connection loss is a request failure state. Do not claim that an unconfirmed review is saved.

These states are documented requirements. They do not have approved mockup images yet.

## Do's and Don'ts

- Use the terms collection, card, cue, key points, review, and grade from CONTEXT.md.
- State what the learner can do next.
- Write errors with a concrete action, such as retry or sign in.
- Keep button labels short and specific.
- Preserve the neutral primary color across light and dark modes.
- Keep button fills flat even when the adjacent cards have depth.
- Use text as well as visual markers for due counts and request states.
- Do not use earlier lime or colored-primary mockups as the current reference.
- Do not add AI assessment, rewards, courses, or graphs to match another app.
- Do not add a color picker under this design scope.
- Do not present a generated screenshot as proof of accessible contrast, responsive behavior, or keyboard support.
- Review unknown measurements during implementation instead of claiming that the mockups supply exact tokens.

## Motion

The approved references are static. Durations and easing curves are unspecified. Do not add card flips, button elevation, or decorative movement without review.

## Dark Mode

Light mode changes the page, sidebar, and surrounding text. Collection cards and key points retain charcoal backgrounds. Dark mode uses lighter neutral selection markers; light mode uses darker markers.

The same primary fill and light label colors apply in both modes. Keep theme changes separate from later primary-color customization.

_Extracted from `main`@`dd4085a` on 2026-10-22._
