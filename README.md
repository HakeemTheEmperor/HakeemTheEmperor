# Toluwalase Akinyemi

**Lead Software Engineer at [Genesis Technologies](https://genesistechnologiesltd.com/). Law student.**

I build reliable APIs, products and developer tooling — mostly TypeScript, Python and Go. My legal training shows up in the work: I care about privacy, correctness and the boring invariants that have to hold when everything happens at once.

[toluwalase.me](https://www.toluwalase.me/) · [Blog](https://www.toluwalase.me/blog) · [LinkedIn](https://www.linkedin.com/in/toluwalase-akinyemi-hte/) · [Résumé](https://www.toluwalase.me/resume.pdf)

*Open to software engineering roles — remote or relocation.*

---

## Open source

Merged upstream:

| Project | Contribution |
|---|---|
| **[Caddy](https://github.com/caddyserver/caddy/pull/8266)** | Fixed TLS config validation that silently accepted invalid curves and `protocol_min`/`protocol_max` values — a config meant to enforce TLS 1.3 could accept TLS 1.2 connections. |
| **[Grafana k6](https://github.com/grafana/k6/pull/6565)** | Fixed `tlsCipherSuites` rejecting the standard IANA names for the ChaCha20 suites, with backward compatibility preserved and regression tests. |
| **[pytest](https://github.com/pytest-dev/pytest/pull/15173)** | Added pretty-printer support so assertion diffs don't print Python 3.15's `frozendict` on a single line, with version-gated tests. |
| **[bitfield/script](https://github.com/bitfield/script/pull/248)** | Added a streaming `Unique()` filter to the Pipe API, in the spirit of Unix `uniq`. |
| **[ESLint](https://github.com/eslint/eslint/pull/21294)** | Documented a scope-resolution limitation in `preserve-caught-error` that can produce false positives. |

Also reported a [PEP 728 TypedDict bug in Pydantic](https://github.com/pydantic/pydantic/issues/13919) where subclasses lost their `closed`/`extra_items` settings and schema generation crashed — root-caused it, maintainer shipped the fix.

> The forked repos below are where this work happens, not bookmarks.

---

## Selected projects

### 🛡️ [Complint](https://github.com/HakeemTheEmperor/compliance-lint) — GDPR static analysis for TS/JS

[![npm](https://img.shields.io/npm/v/complinter.svg)](https://www.npmjs.com/package/complinter)

ESLint, but for legal compliance. Parses your code into an AST and flags privacy risks before they ship — PII in logs, unhashed sensitive fields, unprotected export routes, missing erasure cascades. SARIF 2.1.0 output for CI, inline suppressions, and a plugin API for new rules and languages.

```bash
npm i -D complinter && npx complint src
```

[Case study](https://www.toluwalase.me/projects/complint) · [npm](https://www.npmjs.com/package/complinter)

| Project | What it is | Stack |
|---|---|---|
| **[Kolo Bank Server](https://github.com/HakeemTheEmperor/kolo-bank-server)** | A mock banking core built on a double-entry ledger, with holds and payment workers. Every mutating endpoint takes an idempotency key; external rails are deterministic stubs. Tested under concurrency, retries and process kills. | Go · PostgreSQL · k6 · OpenTelemetry |
| **[iMockMarket](https://github.com/HakeemTheEmperor/trade-sim-backend)** · [live](https://app.imockmarket.toluwalase.me) | A stock-market simulator built as a closed economy — equal starting capital, real broker costs, seasonal leagues — so rankings measure skill, not deposits. [API docs](https://api-imockmarket.toluwalase.me/docs) · [frontend](https://github.com/HakeemTheEmperor/trade-sim-app) | Flask · PostgreSQL · React · WebSockets |
| **[mini-GFS](https://github.com/HakeemTheEmperor/mini-gfs)** | The Google File System, rebuilt small. Files are encrypted client-side, chunked across two chunkservers over gRPC, and re-replicated to a healthy node when one dies. | Go · gRPC · AES-256-GCM · RSA-OAEP |
| **[Ichtaka](https://github.com/HakeemTheEmperor/ichtaka)** · [live](https://ichtaka-app.vercel.app/) | Anonymous incident reporting. Sign-in uses a key derived from a 12-word phrase, so no passwords or emails are ever stored. PII scrubbing in the trust-and-safety path. | FastAPI · PostgreSQL · Next.js |
| **[Socio Kolab](https://github.com/HakeemTheEmperor/socio-kolab)** · [live](https://sk.toluwalase.me/) | White-label portal for student societies — members, dues, events, elections. Each club gets its own URL and colours; authorization is scoped server-side by both resource and club. | Next.js · Prisma · PostgreSQL · Zod |

Closed-source work — [StructHelm](https://app.structhelm.com/) (defect reporting for buildings) and an [enterprise workforce governance API](https://staff.dclm.org/) — is written up at [toluwalase.me/projects](https://www.toluwalase.me/projects).

---

## Where I've worked

- **Genesis Technologies** — Lead Software Engineer (Mar 2026–present). Led the migration from Express/MongoDB to NestJS/PostgreSQL; built oversell protection and an exactly-once document pipeline to accounting.
- **Brane Technologies** — Software Engineer (Dec 2024–Sep 2026). Owned the backend for bill payments, donations and education payments. Held production above 99.5% uptime after taking over reliability.
- **DCLM** — Senior Software Engineer, volunteer (2023–2026). Staff records portal for 2,000+ employees; query work on a 400K+ user membership portal.

Full history and numbers: [toluwalase.me/experience](https://www.toluwalase.me/experience)

---

## Tech

**Languages** TypeScript · JavaScript · Python · Go · SQL
**Backend** NestJS · Node.js · FastAPI · Flask · gRPC · WebSockets
**Frontend** React · Next.js · TanStack Query
**Data** PostgreSQL · MySQL · Prisma · Sequelize · Alembic
**Cloud & DevOps** AWS · Google Cloud · Docker · GitHub Actions · Vercel

---

## Writing

I write about the unglamorous parts of shipping software — broken merges, red CI, staging servers too small to build their own app — over at [toluwalase.me/blog](https://www.toluwalase.me/blog).

## Contact

[toluwalase.akinyemi1@gmail.com](mailto:toluwalase.akinyemi1@gmail.com) · [LinkedIn](https://www.linkedin.com/in/toluwalase-akinyemi-hte/)
