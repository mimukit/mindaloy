# Mindaloy

Mindaloy is a spaced repetition web app that owns its card and review data. This file defines the product and the words its code and documents use.

## Overview

### What it is
Mindaloy is a standalone spaced repetition web app that owns its data. Its API gives agents and other systems the same card and review operations as the web app.

### Who it is for
English-speaking learners and developers who review cards, and the agents and tools that create cards and read progress for them.

### The problem it solves
Learners forget material they do not review on a schedule. The tools that plan their learning have no shared place to put cards and read review results.

### Core capabilities
- Manage collections and the cards in them.
- Review due cards with a typed answer and a grade, scheduled by FSRS.
- Read due cards, review history, and progress.
- Give external clients scoped, revocable API keys.
- Create cards from external clients by external ID, with no duplicates.
- Review cards on a phone through the browser. Offline review with later sync is planned for a later release.

### Non-goals
- No lesson authoring, course management, or learning phase workflow.
- No AI grading, generated cards, or model calls inside Mindaloy.
- No shared collections, organization accounts, or billing.

## Cards and collections

### Owner
The one account that holds a collection and every card and review in it.
_Avoid: user (when ownership is meant), member_

### Collection
A named set of cards with exactly one owner. It is the unit of ownership and of API key scope.
_Avoid: deck, set, folder_

### Card
One thing to learn, made of a cue and its key points, with a stable server ID.
_Avoid: flashcard, note, item_

### Cue
The prompt side of a card, shown before the answer.
_Avoid: question, front, prompt_

### Key points
The answer side of a card. The learner compares a typed answer against it.
_Avoid: answer, back, solution_

### Card revision
The version number of a card's content. It increases on each edit, and each review records the revision it saw.
_Avoid: version, edit count_

### Archived card
A card removed from reviews whose review history stays stored.
_Avoid: deleted card, hidden card_

## Reviews and scheduling

### Review
One immutable record of a learner answering a card: the card revision, the review time, the grade, and a client event ID.
_Avoid: review event, attempt, study session_

### Grade
The learner's own judgement of how well they recalled a card, chosen after the key points are shown. The set is Again, Hard, Good, and Easy, one for each FSRS rating ([ADR 0003](docs/adr/0003-adr-schedule-with-ts-fsrs-on-the-server-2026-10-22.md)).
_Avoid: rating, score, result_

### Schedule
The derived state that says when a card is next due. The scheduler rebuilds it from the card's reviews.
_Avoid: interval, card state_

### Due card
A card whose schedule says it is ready for review now.
_Avoid: pending card, card to study_

### Day start
The local hour, in the owner's time zone, at which a new review day begins. A schedule of one day or more falls due at the day start of its due day.
_Avoid: rollover, midnight, day boundary_

### Pending review
A review saved on a device that the server has not confirmed yet. It exists only with offline review, which is planned for a later release.
_Avoid: unsynced review, queued review, offline review_

### Provisional schedule
A schedule computed on a device from pending reviews. The server schedule replaces it after sync. It exists only with offline review, which is planned for a later release.
_Avoid: local schedule, temporary schedule_

## Integration

### External client
Any system other than the Mindaloy web app that uses the API with an API key, such as an agent.
_Avoid: integration, third-party app, bot_

### External ID
The pair of an external source ID and an external card ID that an external client gives a card. It is unique within a collection, so a repeated create does not make a duplicate card.
_Avoid: foreign key, client ID, source key_

### API key scope
The set of operations and the list of collections that one API key may use. A request outside either one is refused.
_Avoid: permission, role, access level_
