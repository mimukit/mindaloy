# Mindaloy page mockups

Created: 2026-10-22

Status: Draft 01. The owner approves the page list and collection forms. The page images still need approval.

The built-in imagegen tool creates these static references. Each image includes a desktop layout and a phone layout. The [design system](../../../DESIGN.md) supplies the approved palette, card treatment, and font roles.

Use Newsreader for the wordmark, headings, collection names, and review cues. Use DM Sans for body text and controls. Generated lettering approximates these fonts. The [font comparison](../mindaloy-font-comparison.html) supplies the exact font specimens.

The [review gallery](index.html) uses smaller JPEG copies in `previews/`. The links below open the original PNG files.

## Images and prompts

| Page | Dark image | Light image | Dark prompt | Light prompt |
|------|------------|-------------|-------------|--------------|
| Sign in | [Image](01-sign-in-dark-v1.png) | [Image](01-sign-in-light-v1.png) | [Prompt](01-sign-in-dark-v1-prompt.txt) | [Prompt](01-sign-in-light-v1-prompt.txt) |
| Collections | [Image](02-collections-dark-v1.png) | [Image](02-collections-light-v1.png) | [Prompt](02-collections-dark-v1-prompt.txt) | [Prompt](02-collections-light-v1-prompt.txt) |
| Collection detail | [Image](03-collection-detail-dark-v1.png) | [Image](03-collection-detail-light-v1.png) | [Prompt](03-collection-detail-dark-v1-prompt.txt) | [Prompt](03-collection-detail-light-v1-prompt.txt) |
| Card editor | [Image](04-card-editor-dark-v1.png) | [Image](04-card-editor-light-v1.png) | [Prompt](04-card-editor-dark-v1-prompt.txt) | [Prompt](04-card-editor-light-v1-prompt.txt) |
| Review | [Image](05-review-dark-v1.png) | [Image](05-review-light-v1.png) | [Prompt](05-review-dark-v1-prompt.txt) | [Prompt](05-review-light-v1-prompt.txt) |
| Card detail and review history | [Image](06-card-detail-dark-v2.png) | [Image](06-card-detail-light-v2.png) | [Prompt](06-card-detail-dark-v2-prompt.txt) | [Prompt](06-card-detail-light-v2-prompt.txt) |
| Integration settings | [Image](07-integration-settings-dark-v1.png) | [Image](07-integration-settings-light-v1.png) | [Prompt](07-integration-settings-dark-v1-prompt.txt) | [Prompt](07-integration-settings-light-v1-prompt.txt) |

Card detail uses Draft 02. This revision corrects the cue label, key-points font role, and secondary actions. Draft 01 files remain as earlier records.

## Page boundaries

- Sign in uses the owner's email and password. The first release has no registration or password reset email.
- Collections includes the collection creation form. Collection detail includes the collection edit form. Neither form needs a separate page.
- Collection detail contains the card list, search, archive filter, and review action for that collection.
- Card editor uses the same layout for creation and edits. An edit keeps the existing schedule.
- Review separates recall, reveal, and completion. The learner selects a grade after reveal. The app preserves the typed answer.
- Card detail shows key points, schedule data, and review history with retained typed answers.
- Integration settings shows key names, collection scopes, operation scopes, last use, creation, and revocation. The app displays a new key once.

The collection form name field is a starting proposal. Deletion, archive confirmation, schedule reset confirmation, and request failure states need further state references.

## Review requirements

Sample counts and content do not represent real activity. The integration mockup uses a nonfunctional demonstration key.

Compare each page in both themes before approval. Check the collection forms, text hierarchy, phone layout, and action labels. Keep buttons flat during implementation even if generated pixels contain residual highlights.

These images do not verify keyboard behavior, font metrics, contrast, or responsive code. The approved scope in issue #1's branch excludes offline reviews and sync.

Create one implementation issue per page after the owner approves its references. Record the approved image paths and required states in each issue.
