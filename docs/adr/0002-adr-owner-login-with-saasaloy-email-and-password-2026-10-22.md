# 0002: Owner login with Saasaloy email and password

The first deployment serves one owner, and it runs on the Workers free tier with no paid email service. The owner logs in to the web app with email and password through Saasaloy's `auth` module (Better Auth, sessions in D1). A seed command creates the owner account, and sign-up is off from the first deploy. External clients never use this login; they use scoped API keys.

## Status
accepted

## Considered Options
- Cloudflare Access in front of the web routes. It needs no login code, but it moves identity outside the app and outside Saasaloy.
- Magic link by email. Saasaloy's `auth` module has no magic link, and sending mail on the free tier needs an outside vendor such as Plunk.
- Passkeys built into the Worker. No outside dependency, but about a phase of auth work and a recovery path to design.

## Consequences
- Saasaloy's `auth` module lets the first account to sign up become superadmin. Mindaloy's copy of `auth.ts` sets `emailAndPassword.disableSignUp: true`, and `pnpm db:seed:owner` creates the owner from `OWNER_EMAIL`. This one line differs from the Saasaloy module, so a later `saasaloy add` that rewrites `auth.ts` must keep it.
- Better Auth hashes passwords with scrypt. The free tier allows 10 ms of CPU per request, and no Saasaloy file shows that sign-in fits. Phase 3 measures it, and an overrun stops the phase.
- With no email sender there is no reset email. The owner resets the password with a script that writes a new hash to D1.
