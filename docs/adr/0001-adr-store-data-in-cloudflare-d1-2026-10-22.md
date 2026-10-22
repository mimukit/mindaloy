# 0001: Store data in Cloudflare D1

The first release must run entirely on the Cloudflare Workers free tier, so the draft plan's PostgreSQL choice no longer fits. Mindaloy stores accounts, collections, cards, reviews, schedules, and API keys in one Cloudflare D1 (SQLite) database, with the schema in Drizzle ORM and migrations through Saasaloy's `database-d1` module. D1 binds to the Worker directly, needs no outside host, and is the database Saasaloy already ships a driver for.

## Status
accepted

## Considered Options
- PostgreSQL on an outside free tier (for example Neon) reached through Hyperdrive. It keeps PostgreSQL features, but the app is then not all on Cloudflare, and a free outside database sleeps when idle.

## Consequences
- The free tier sets hard limits: 500 MB per database, 5 million rows read and 100,000 rows written per day, and 50 queries per Worker request. One owner stays far under them, but batch endpoints are capped at 50 cards per request.
- SQLite has no row locks and no `jsonb`. A review and its derived schedule are written in one D1 `batch()` so they commit together.
- Restore relies on D1 Time Travel, which keeps 7 days on the free plan, plus a weekly `wrangler d1 export` the owner runs by hand. A cron Worker cannot dump the database within 10 ms of CPU.
