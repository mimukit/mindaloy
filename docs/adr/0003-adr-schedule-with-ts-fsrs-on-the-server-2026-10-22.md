# 0003: Schedule with ts-fsrs on the server

Every schedule is derived from reviews, so the scheduler and its settings must be reproducible. Mindaloy schedules cards with `ts-fsrs` in one server module, using the FSRS default parameters and a desired retention of 0.90. Each review points to a `scheduler_config` row that holds the `ts-fsrs` version, the parameter weights, and the retention, so a replay of a card's reviews always gives the same schedule.

## Status
accepted

## Considered Options
- A fixed SM-2 style scheduler. It is simpler, but it ignores how late a review was and goes against the settled FSRS choice.
- Running the FSRS parameter optimizer from the start. It needs about 1,000 reviews before it helps, and it needs far more than the 10 ms of CPU a free-tier Worker request allows.

## Consequences
- The four grades map 1:1 to FSRS ratings: Again 1, Hard 2, Good 3, Easy 4. Reviews store the rating as an integer.
- Personal parameters can come later with no schema change: the owner runs the optimizer outside the Worker and saves the result as a new `scheduler_config` row.
- The scheduler runs only on the server. A later offline release computes a provisional schedule on the device, and the server schedule replaces it after sync.
- A replay runs one card per request so it stays inside the Worker CPU limit. A rebuild of a whole collection must be split across requests.
