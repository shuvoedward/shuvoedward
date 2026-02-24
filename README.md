# Cornelius Edward

Fullstack Software Engineer with a backend focus. I build production-ready systems in Go — REST APIs, caching layers, job schedulers, search, and cloud deployment. Frontend experience in React and JavaScript.

Currently based in Queens, NY. Actively looking for backend or fullstack engineering roles.

---

## What I'm Building

### [Bible Notes API](https://github.com/shuvoedward/Bible_project_2) — Live at [biblenotesapi.dev/v1/healthcheck](https://biblenotesapi.dev/v1/healthcheck)

A production API I designed and built end-to-end — from schema design and user flows to deployment on AWS EC2. Not a tutorial follow-along. I made the product decisions, hit the real problems, and figured them out.

**Stack:** Go, PostgreSQL, Redis, Docker, AWS EC2/S3, Caddy

**What's under the hood:**
- **Rate limiting** — sliding window algorithm using Redis + a Lua script for atomic enforcement across multiple tiers
- **Concurrency safety** — singleton pattern with [Otter](https://github.com/maypok86/otter) to handle concurrent requests hitting the same Bible passage without redundant DB calls
- **Full-text search** — PostgreSQL `tsvector`/`tsquery` for keyword and partial-phrase verse search
- **Autocomplete** — in-memory Go map for instant book lookup without touching the database
- **Image processing** — resizes oversized uploads before storing to AWS S3
- **Job scheduler** — custom-built with goroutines, worker pool, and a min-heap priority queue for retries; currently drives email delivery
- **Auth** — token-based authentication with Redis caching to cut redundant DB reads
- **Testing** — writing integration and unit tests; previously load tested with k6 (51k req/sec on verse retrieval)

> Performance numbers, architecture notes, and design decisions are documented in [DESIGN.md](https://github.com/shuvoedward/Bible_project_2/blob/main/DESIGN.md) and [docs/](https://github.com/shuvoedward/Bible_project_2/tree/main/docs).

---

### [Flashcard Web App](https://github.com/shuvoedward/Flashcard)

**Stack:** React, JavaScript

A responsive flashcard interface built with component-based architecture and state management. Covers navigation, dynamic rendering, and multi-state card logic.

---

## Open Source

Currently studying the [k6](https://github.com/grafana/k6) and [Gitea](https://github.com/go-gitea/gitea) codebases — reading production-level Go at scale, understanding architecture and contributing patterns. Working toward first contributions.

---

## Skills

| | |
|---|---|
| **Languages** | Go, SQL, JavaScript |
| **Backend** | REST APIs, rate limiting, background jobs, job scheduling, image processing |
| **Databases** | PostgreSQL (full-text search, indexing, query optimization), Redis |
| **Frontend** | React, ES6 |
| **Cloud & DevOps** | AWS EC2, S3, Docker, Linux, Caddy |
| **Tools** | Git, Postman, k6, Otter |
| **Concepts** | Concurrency patterns, data structures & algorithms, transactions, secure coding |

---

## Background

Self-taught, with CS coursework at BMCC (2022–2024) covering Data Structures, Algorithms, Databases, and Operating Systems. I learn by building real things and reasoning from first principles — not following tutorials.

---

## Get in Touch

- Email: shuvoedward@gmail.com
- LinkedIn: [linkedin.com/in/cornelius-edward-1b5b03214](https://www.linkedin.com/in/cornelius-edward-1b5b03214/)
