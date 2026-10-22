# Plan: Mindaloy visual direction for issue #2

Created: 2026-10-22

Status: The owner approves the final concept 05 flat-control mockups on 2026-10-22. [DESIGN.md](../../DESIGN.md) records the system. The owner approves the integration settings Draft 01 on 2026-10-22, which completes the screen coverage of issue #2.

The final approval covers desktop collections and phone review after reveal in dark and light modes. It supersedes the earlier lime, colored-primary, and raised-button variations. The design document records phone behavior, keyboard guidance, and request states. Those rules do not represent browser test results.

The owner selects concept 05 instead of the later layout variations. Keep its layout, backgrounds, card colors, and controls. Apply the approved Newsreader and DM Sans font selection below. Replace lime with neutral charcoal. Defer user-selectable primary colors to later theme support. This selection does not complete issue #2.

The owner requests flat buttons after reviewing the neutral edits. Apply the same button treatment in dark and light modes. Remove gradients, bevels, reflective edges, and shadows from primary actions, grade controls, and selected navigation. Keep the accepted depth on collection cards and the key-points card.

## Approved fonts

The owner selects option 2, Newsreader with DM Sans, on 2026-10-22. Use Newsreader for the wordmark, headings, collection names, and review cue. Use DM Sans for navigation, body text, counts, labels, and controls. Apply this pair in light and dark modes.

The [font comparison](../../output/design/mindaloy-font-comparison.html) preserves all five alternatives. This selection replaces the unspecified fonts in the approved images. Font sizes, weights, line heights, and letter spacing still require specification.

## Page coverage update

The owner approves seven starting pages and collection forms on 2026-10-22. The pages are Sign in, Collections, Collection detail, Card editor, Review, Card detail with review history, and Integration settings.

Collection creation uses a form within Collections. Collection editing uses a form within Collection detail. Neither form needs a separate page.

The owner requests light and dark mockups for every page. The [page review index](../../output/design/pages/README.md) links the images and generation prompts. The built-in imagegen tool creates these drafts. Each image shows desktop and phone layouts.

The integration settings images are approved on 2026-10-22. The other page images remain drafts, and each page issue (#3 to #9) settles its own reference during planning. They do not replace the approved concept 05 references.

## Selected starting point

Use [dark concept 05](../../output/design/mindaloy-dark-concept-05.png) for the layout and card treatment. Its [prompt](../../output/design/mindaloy-dark-concept-05-prompt.txt) records the source references.

The [new light reference](../../output/design/references/owner-04-light-palette.jpg) uses a light gray background with charcoal book covers. The light mockup keeps charcoal collection cards and a charcoal key-points card. Change the application background, sidebar, and text outside cards to the light palette. Preserve the composition, type, controls, and sample content from concept 05.

Propose light page `#DEDEDC`, sidebar `#D2D2D0`, outside text `#30302E`, secondary text `#62625E`, and charcoal cards `#3A3A3A`. The current primary action uses a flat charcoal `#3A3A3A` fill with off-white text `#ECECE6` in both modes. A single uniform gray stroke `#666666` can define its edge. Do not add a reflective rim or shadow. These values guide the image edit. They are not a final token specification.

Use a neutral light gray marker `#B6B6B0` for selected navigation and progress on dark pages. Use dark gray `#4A4A48` for these markers on light pages. Keep due dots on charcoal cards light gray. This preserves visible state without a colored accent.

The built-in imagegen tool makes targeted neutral edits of both selected images. Keep the earlier lime images as records of the color exploration.

The next variation removes the raised button treatment. The built-in imagegen tool edits each neutral image. Keep the neutral images above as earlier references.

| Mode | Flat-control reference | Edit prompt |
|------|------------------------|-------------|
| Dark | [Image](../../output/design/mindaloy-dark-concept-05-flat-controls.png) | [Prompt](../../output/design/mindaloy-dark-concept-05-flat-controls-prompt.txt) |
| Light | [Image](../../output/design/mindaloy-light-concept-05-flat-controls.png) | [Prompt](../../output/design/mindaloy-light-concept-05-flat-controls-prompt.txt) |

| Mode | Neutral reference | Edit prompt |
|------|-------------------|-------------|
| Dark | [Image](../../output/design/mindaloy-dark-concept-05-neutral.png) | [Prompt](../../output/design/mindaloy-dark-concept-05-neutral-prompt.txt) |
| Light | [Image](../../output/design/mindaloy-light-concept-05-neutral.png) | [Prompt](../../output/design/mindaloy-light-concept-05-neutral-prompt.txt) |

The light image does not add a theme selector or a primary-color setting. User-selectable primary colors remain later work.

The built-in imagegen tool creates [light concept 05](../../output/design/mindaloy-light-concept-05.png) by editing dark concept 05 with the supplied light reference. The [edit prompt](../../output/design/mindaloy-light-concept-05-prompt.txt) records the palette and preserved content. The owner accepts its layout and requests replacement of the lime accent.

## Earlier layout and color comparison

Preserve concept 05's charcoal backgrounds, gray cards, rounded edges, and subtle depth. Compare layouts and action colors only. Keep the phone review content consistent. Each image includes a separate light and dark button specimen. The application screens remain dark.

| Concept | Desktop layout | Primary button fill | Accent text on dark | White button text contrast |
|---------|----------------|---------------------|---------------------|----------------------------|
| 06 | Narrow icon rail and horizontal collection rows | Blue `#5267D8` | `#A9B7FF` | 4.89:1 |
| 07 | Top navigation and landscape collection cards | Violet `#8058C7` | `#CBB0FA` | 5.07:1 |
| 08 | Split collection browser and selected collection | Teal `#227C73` | `#86D5C8` | 5.00:1 |

Use the same primary button fill with white text in light and dark modes. Use the lighter tint for small colored text on dark backgrounds. The primary fills alone do not provide sufficient contrast for small text on charcoal.

Calculate these ratios from the specified sRGB values using the WCAG relative luminance formula. Each white label exceeds the [4.5:1 requirement for normal text](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), checked on 2026-10-22. This calculation covers the proposed solid button fills. Generated images can vary from exact tokens and do not prove complete UI accessibility.

The generated images and exact prompts stay together.

| Concept | Image | Prompt |
|---------|-------|--------|
| 06, blue | [Image](../../output/design/mindaloy-dark-concept-06.png) | [Prompt](../../output/design/mindaloy-dark-concept-06-prompt.txt) |
| 07, violet | [Image](../../output/design/mindaloy-dark-concept-07.png) | [Prompt](../../output/design/mindaloy-dark-concept-07-prompt.txt) |
| 08, teal | [Image](../../output/design/mindaloy-dark-concept-08.png) | [Prompt](../../output/design/mindaloy-dark-concept-08-prompt.txt) |

The owner selects concept 05 after this comparison. Keep concepts 06 to 08 as earlier alternatives. Concept 08 needs clearer separation between the selected collection's 12 due cards and the action for all 24 cards. It also adds serif type to the selected collection name.

## Current visual brief

The owner's supplied images now guide the visual style. Mochi remains a structural research reference. The earlier mockups do not define the current direction.

| Supplied reference | Details to use | Boundary |
|--------------------|----------------|----------|
| [Dream journal](../../output/design/references/owner-01-dream-journal.jpg) | Charcoal layers, stacked cards, rounded controls, and serif headings. | Do not add recording or a calendar. |
| [Node canvas](../../output/design/references/owner-02-node-canvas.jpg) | Quiet tonal depth and thin edges. | Do not add a node editor or a background grid to review content. |
| [Sidebar](../../output/design/references/owner-03-sidebar.jpg) | Raised selected navigation, inset icons, subtle highlights, and a small lime marker. | Do not copy its product name or video features. |

Use the sidebar reference as the primary desktop style reference. Propose serif type for the review cue from the journal reference. Keep labels and controls in sans-serif type. These are design interpretations for the next mockup, not final approval.

Keep subtle tonal depth on collection cards and the key-points card. All buttons use flat fills without gradients, bevels, or shadows. Keep the page background quiet. Propose charcoal `#1A1A1A`, sidebar `#202020`, card layers near `#303030`, and text `#EAEAE5`. The current primary color follows the neutral specification above. These values are visual estimates, not sampled colors or final tokens.

The built-in imagegen tool creates [concept 05](../../output/design/mindaloy-dark-concept-05.png) with all three supplied images as style references. The [prompt](../../output/design/mindaloy-dark-concept-05-prompt.txt) records their separate roles. The concept shows desktop collections and a phone review after reveal. The owner selects it as the starting point. Preserve its serif desktop headings and review cue in the light edit.

## Earlier concepts

The owner rejects concept 01 and requests three more minimal, modern variations. Keep dark mode. Reduce borders, remove nested panels, and simplify grade controls. Compare a graphite sidebar layout, warm editorial top navigation, and a compact slate layout. None has visual approval.

The built-in imagegen tool creates these variations on 2026-10-22. Each shows the same desktop collection list and phone review after reveal. Sample counts and content are placeholders.

| Concept | Image | Generation prompt |
|---------|-------|-------------------|
| 02, borderless graphite | [Image](../../output/design/mindaloy-dark-concept-02.png) | [Prompt](../../output/design/mindaloy-dark-concept-02-prompt.txt) |
| 03, warm editorial | [Image](../../output/design/mindaloy-dark-concept-03.png) | [Prompt](../../output/design/mindaloy-dark-concept-03-prompt.txt) |
| 04, compact slate | [Image](../../output/design/mindaloy-dark-concept-04.png) | [Prompt](../../output/design/mindaloy-dark-concept-04-prompt.txt) |

Concepts 02 to 04 are rejected. Keep them as records of earlier exploration. They do not prove phone target sizes or accessibility.

First concept: [dark collection and review mockups](../../output/design/mindaloy-dark-concept-01.png). The built-in imagegen tool creates this concept on 2026-10-22. The [generation prompt](../../output/design/mindaloy-dark-concept-01-prompt.txt) records the proposed colors and content. The image shows desktop collections, a desktop review before reveal, and a phone review after reveal. Integration settings and the phone keyboard state still need references. Generated shading does not define final color tokens.

## Context

[Issue #2](https://github.com/mimukit/mindaloy/issues/2) requires approved references for the collection list, review screen, and integration settings. It also requires DESIGN.md and a dated approval in the product plan. This document plans that work before application UI starts.

Mindaloy serves English-speaking learners and developers. External clients create cards through its API. The web app supports typed answers and self-assessed grades. Success means the owner can approve the same visual system across all required screens and phone layouts.

The repository has no application code or DESIGN.md. The product plan is `docs/plans/0001-plan-mindaloy-2026-10-21.md`. `CONTEXT.md` defines the product terms.

The issue #1 branch contains newer approved scope than this checkout. The branch is `issue-1-settle-mindaloy-first-release-scope-and-stack`, inspected at `078b0cd`. It defines online phone reviews, four grades, and API key scopes. Recheck that branch before final approval. Do not restore offline reviews from the older plan in this checkout.

## Design decisions (settled)

| Decision | Resolution |
|----------|------------|
| Work boundary | Research and visual planning precede application UI. The owner approves the reference. |
| Required screens | Collection list, review screen, and integration settings, as specified in issue #2. |
| Product terms | Use collection, card, cue, key points, review, and grade from CONTEXT.md. |
| Initial visual direction | The owner selects a dark variation based on Mochi's UI and UX on 2026-10-22. |
| Current style references | The owner supplies three images on 2026-10-22. Use them for the next visual exploration. |
| Starting concept | The owner selects concept 05 on 2026-10-22 and requests a light counterpart from a supplied palette reference. |
| Default primary color | The owner selects grayish black on 2026-10-22. Use charcoal buttons with light text in both modes. |
| Button treatment | The owner requests flat controls in both modes. Remove gradients, bevels, highlights, and shadows from buttons. Preserve card depth. |
| Font families | The owner selects Newsreader with DM Sans on 2026-10-22. |
| Later themes | Defer user-selectable primary colors. |
| Approval status | The owner accepts concept 05's dark and light layouts with the neutral primary-color change. The integration settings Draft 01 is approved on 2026-10-22. Other page drafts are settled in their own issues. |

## Research

Research date: 2026-10-22. Sources are official product pages and documentation. Browser inspection covers public pages and public product images. Mochi also exposes an anonymous app view. No account creation, paid access, or complete authenticated review test occurs.

Visual descriptions below are observations. The proposed lessons for Mindaloy are design judgments. Public screenshots can differ from the current authenticated product. Exact competitor color values are not measured.

| App | Evidence and observed direction | Use in Mindaloy | Limit |
|-----|---------------------------------|-----------------|-------|
| [Mochi](https://mochi.cards/) | The anonymous app shows a narrow sidebar, muted controls, and a large content area. Its [API documentation](https://mochi.cards/docs/api/) places key management in account settings. | Use restrained navigation and direct access to collections. Keep API key management easy to find. | The anonymous view has no populated card content during inspection. It does not prove the full review process. |
| [RemNote](https://www.remnote.com/feature/spaced-repetition) | Public product images show collection hierarchy and due counts. Its [review guide](https://help.remnote.com/en/articles/6022755-getting-started-with-spaced-repetition) describes reveal, four ratings, keyboard controls, and optional typed answers. | Show due counts beside collection names. Separate recall, reveal, and grade. | Its notes, exam tools, and nested structure exceed Mindaloy's first-release scope. |
| [JustFlip](https://just-flip.app/index.html) | Public phone images show dark cards and large text. The site presents an editorial collection list, swipe review, and four grades. | Keep phone reviews focused. Place explicit grade buttons within reach. | Swipes must not replace visible buttons. Native Apple layouts do not directly define a browser layout. |
| [Soma](https://www.studysoma.com/) | The site identifies an early-access Mac app. Public images use bright blue, rounded cards, and a separate review view. The product includes mascots and rewards. | Explore a more playful brand through color and restrained shapes. | Do not add mascot care, a shop, or reward mechanics without a separate product decision. |
| [Recall](https://www.recall.it/) | Public images use a thumbnail library. Its [review documentation](https://docs.recall.it/deep-dives/quiz-and-spaced-repetition) describes a focused session, progress, typed answers, and review counts. | Keep session progress visible. Make source context secondary to the cue. | AI generation, knowledge stages, graphs, and challenges do not belong in this visual scope. |

[Traverse](https://traverse.link/) combines maps, notes, and reviews. Its map structure does not fit the current collection model. [Voovo](https://www.voovostudy.com/) presents courses, adaptive practice, and an AI tutor. Its course structure does not fit the first release. Neither provides a closer primary reference than Mochi.

Mochi is the strongest structural reference. RemNote supplies useful review behavior. JustFlip supplies phone composition ideas. Combine these lessons in an original reference rather than copy one product.

## Approach

Use the supplied references for charcoal layers, restrained depth, and rounded controls. Keep the selected concept's stacked collection cards and neutral charcoal primary color. Give the cue and typed answer most of the review area. Keep grade meanings independent of the brand palette.

The first comparison uses a single dark direction across desktop collections and desktop and phone reviews. Exact colors remain proposals. The earlier light palette options remain alternatives if the owner requests them. A more playful direction requires another brand decision.

Reuse the screen requirements from issue #2 and the product terms from CONTEXT.md. Use issue #1's latest decisions for the grade set and API key controls. Do not select a component library through this research.

### Phase 1: select a brand direction

Attended: The owner selects the exact palette. The initial dark direction is selected on 2026-10-22.

- Use the supplied references for the next dark variation.
- Propose background `#1A1A1A`, sidebar `#202020`, and raised controls `#303030`.
- Propose main text `#EAEAE5` and secondary text `#A8A8A2` for dark mode. Use the neutral primary-color specification above.
- Treat these values as original proposals, not sampled competitor colors.
- Compare typography, spacing, corner shapes, and control density alongside the colors.
- Use dark mode for the first reference. Decide final theme coverage later.

Done when: This document records the selected direction and the owner's decision date.

### Phase 2: compare mockup images

Attended: The owner chooses a mockup direction and requests changes.

- Generate the first dark concept with sample collection content and due counts.
- Include a desktop collection list and a phone review in each first comparison.
- Show the cue, a typed answer, and revealed key points in separate review states.
- Show Again, Hard, Good, and Easy after reveal, in that order.
- Use placeholder values for counts and sample content. Do not imply real progress data.
- Expand the selected direction into the integration settings screen.
- Show API key name, collection access, operation access, last use, and revocation controls.
- Show the new key once, with a copy control and a clear instruction to save it.
- Save the images and generation prompts with stable paths before final approval.

Done when: The owner can compare the directions and inspect all three required screens in the selected direction.

### Phase 3: specify interaction and request states

Attended: The owner approves phone behavior and the review controls.

- Define desktop and phone layouts for collections and integration settings.
- Define phone review layouts before and after reveal, including the open software keyboard.
- Propose a single review column on phones and a two-by-two grade button layout.
- Propose Ctrl+Enter or Cmd+Enter to reveal from the answer field. Keep Enter available for a new line.
- Propose number keys 1 to 4 for grades after reveal. Suppress them while the user edits text.
- Define focus order and visible focus. Move focus to an appropriate control after reveal and after save.
- Define loading, no collections, no due cards, request failure, and expired session states.
- Define connection loss as a request failure. Keep the current answer visible and provide retry.
- Advance after server confirmation. Prevent repeated clicks while a request is pending.
- Preserve the client event ID when a review request needs a retry.
- Specify readable contrast and targets of at least 44 by 44 CSS pixels for phone controls.
- Check text, focus indicators, and semantic colors separately from the palette samples.
- Keep full offline review and sync states outside this release, subject to the final issue #1 scope.

Done when: A reviewer can trace recall, reveal, grade, save, and retry with both a keyboard and phone controls.

### Phase 4: record the approved reference

Attended: The owner explicitly approves dated images for every required screen.

- Write DESIGN.md from the selected images and accepted interaction rules.
- Record palette roles, typography, spacing, control states, and phone layouts.
- Link the exact image files and record the approval date.
- Add the dated visual approval to the current product plan after the issue #1 changes are available.
- Check every acceptance item in issue #2 against the files.

Done when: DESIGN.md records the approved rules and reference paths. The product plan records the owner's approval date.

## Open questions

- Do the neutral edits preserve the accepted dark and light compositions?
- Does the first release include both light and dark modes? Both are now part of the visual exploration.
- Does the owner want a small brand illustration, or only type and color?
- Does the owner accept the proposed review shortcuts and phone grade layout?
- How do the final API contract and app shell affect the integration settings layout?

## Non-goals

- No application UI, component implementation, or dependency installation.
- No inferred visual approval, issue closure, commits, or deployment.
- No AI answer assessment, course tools, reward system, or expanded scheduling scope.
- No claim that public screenshots prove accessibility or authenticated product behavior.
