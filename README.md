# Mindaloy

Mindaloy is a spaced repetition web app that owns its own card and review data. Its API gives agents and other tools the same operations the web app uses, so they can add cards and read back how the reviews went.

## Why

People forget what they study unless they come back to it on a schedule. The tools that plan someone's learning, an agent included, also need somewhere to put cards and a way to see what stuck. Mindaloy is that place: you review in the browser or on your phone, and other systems work with the same data through the API.

## What it does

- Keeps cards in collections. A card has a cue on one side and key points on the other.
- Shows the cards that are due. You type an answer, compare it with the key points, and grade yourself. FSRS decides when the card comes back.
- Reports due cards, review history, and progress.
- Issues revocable API keys, scoped to specific operations and collections.
- Accepts cards from external clients by external ID, so sending the same card twice does not create a duplicate.
- Lets you review on a phone without a connection and syncs the results later.

It does not author lessons, grade answers with AI, generate cards, or share collections between accounts. An external agent can generate cards and send them in through the API.

[CONTEXT.md](CONTEXT.md) defines the terms used across the code and docs.

## Status

Mindaloy is in planning, and there is no application code yet. The draft plan is [docs/plans/0001-plan-mindaloy-2026-10-21.md](docs/plans/0001-plan-mindaloy-2026-10-21.md). It proposes TypeScript for the API and web client, PostgreSQL for storage, and a PWA for offline reviews. Phase 1 of the plan still has to approve the stack and the first-release scope.

## Install and run

Setup steps will go here once the stack is chosen.

## License

[MIT](LICENSE)
