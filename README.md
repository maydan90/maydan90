# Hi, I'm Yurii

Backend-leaning full-stack engineer in Jacksonville, FL. TypeScript (Effect), Python, PostgreSQL, AWS.

Until October 2026 I was a senior software engineer at [Maple](https://maple.inc), a restaurant-tech startup with an LLM phone agent and a platform for ordering, payments and reservations. That work lives in private repos, so here is the shape of it.

## Selected work

- **Public Developer API**: designed and shipped Maple's partner API: OAuth 2.0 client credentials and scoped keys, test/live isolation, an order decision loop, HMAC-signed webhooks with durable delivery and replay, a sandbox and a self-service partner console. Closed every critical finding of the pre-launch security audit. The docs are generated from OpenAPI and are public: [docs.maple.inc/developer-api](https://docs.maple.inc/developer-api/overview) · [changelog](https://docs.maple.inc/developer-api/changelog) · [Postman](https://docs.maple.inc/developer-api/postman)
- **Reservations platform**: a ground-up rebuild: native availability engine, durable OpenTable integration (leased operations, idempotent replay, recovery of unknown outcomes), waitlist, host tools, an SVG floor-plan editor. Treating provider refusals as final removed about 6k wasted retries a week.
- **Voice-agent integration**: the backend an LLM phone agent calls at ~7k calls a day: typed, speakable tool outcomes in place of raw provider errors and per-change request IDs reused on retry, which ended retry loops and double-bookings; contributed to the Python agent itself (LiveKit Agents) on its reservation tool.
- **Payments**: CyberSource Unified Checkout and automated merchant boarding on TSYS, Worldpay and Fiserv; Evervault tokenization; earlier, Stripe billing and payouts.
- **SMS compliance**: a Twilio A2P 10DLC registration platform with webhook automation and nightly self-healing, and deliverability fixes that took carrier-blocked payment reminders from ~38% to zero.
- **Platform**: made the initial commit of the monorepo (SST on AWS, Bun, Turbo) and the first backend services.

## Public work

Three repos built in October 2026 as from-scratch demonstrations of patterns I used in private codebases, written with Claude Code as a pair and reviewed, tested and committed by me. Nothing in them is taken from an employer's code.

- [durable-integrations](https://github.com/maydan90/durable-integrations): idempotency keys, leased operations, recovery from unknown outcomes and webhook delivery with replay, in TypeScript on PostgreSQL, tested against a real database.
- [voice-booking-agent](https://github.com/maydan90/voice-booking-agent): a LiveKit Agents voice agent for appointment booking, with typed speakable tool outcomes, per-change request ids reused on retry, and deterministic evals that replay tool calls without an LLM.
- [design-notes](https://github.com/maydan90/design-notes): short write-ups of designs and incidents from integrations, payments and an LLM phone agent.

## How I work

Ticket → branch → PR with test evidence → CI green and every review thread closed. Integration tests against a real Postgres, recording fakes for vendors, contract tests pinned to payloads production accepted. Logs that let you file a vendor ticket without reproducing anything. Coding agents daily, with their PRs reviewed the same way as a person's.

## Contact

maydan90@gmail.com · [LinkedIn](https://www.linkedin.com/in/yurii-maidaniuk)
