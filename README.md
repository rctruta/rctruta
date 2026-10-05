### Ramona C. Truta

Hi, I'm Ramona, an Independent Researcher, Solutions Architect and [Educator](https://ramonactruta.com/teaching.html). I bring over 20 years of rigorous [database engineering](https://ramonactruta.com/work.html#data-engineering) experience to the world of AI; my current focus is on [System Integrity](https://ramonactruta.com/work.html)—applying the strict determinism of data engineering to the probabilistic nature of [AI Agents](https://ramonactruta.com/work.html#agent-evaluation). More to the point, I build [instruments that measure](https://ramonactruta.com/work.html#benchmarking) whether database and AI agents do, and then [publish the experiment alongside the result](https://ramonactruta.com/writing.html). In that way, you can [reproduce it](https://github.com/rctruta/sql-benchmarks-dagster) or show me where I'm wrong. This site is built the same way: generated from data, and the build fails on an unknown tag, a broken anchor, or an unregistered number.

[Portfolio](https://ramonactruta.com) · [Writing](https://ramonactruta.substack.com) · [LinkedIn](https://linkedin.com/in/ramonactruta) · [ORCID](https://orcid.org/0009-0008-4886-7777)

---

#### sqlbenchdag — a reproducible SQL benchmarking laboratory

[**sql-benchmarks-dagster**](https://github.com/rctruta/sql-benchmarks-dagster) · `pip install sqlbenchdag` · [MCP server in the official registry](https://mcpverzeichnis.com/en/server/io-github-rctruta-sqlbenchdag)

Every experiment is a capsule addressed by an 8-character SHA-256 fingerprint over its config,
SQL, and every line of measurement-relevant Python. Change the method, the ID changes.
Cold-cache execution, hard row-count assertions, an integrity seal on every capsule — and
OpenTimestamps proofs anchored to Bitcoin on the four published Quack capsules.

| Finding | Capsule |
|---|---|
| DuckDB-over-Quack (pushdown) beats PostgreSQL at every scale past the noise floor — 4.4× @100K, 6.1× @1M, 13.2× @10M rows | [`902d1277`](https://github.com/rctruta/sql-benchmarks-dagster/tree/main/sql_benchmarks/experiments/results/902d1277) |
| Attach-mode overhead grows with scan size (2.6× @100K → 9.5× @10M); pushdown stays flat at ~2× | [`b8e2bfaf`](https://github.com/rctruta/sql-benchmarks-dagster/tree/main/sql_benchmarks/experiments/results/b8e2bfaf) |
| That flat ~2× residual is reduced server-side parallelism, not protocol transport | [`25b0e134`](https://github.com/rctruta/sql-benchmarks-dagster/tree/main/sql_benchmarks/experiments/results/25b0e134) |
| Attach mode cannot execute multi-table joins at all; pushdown holds ~1.8× on a 3-way TPC-H join | [`b198363e`](https://github.com/rctruta/sql-benchmarks-dagster/tree/main/sql_benchmarks/experiments/results/b198363e) |

[Full published-capsule index →](https://github.com/rctruta/sql-benchmarks-dagster/blob/main/docs/published_capsules.md)

---

---

### Projects

#### Data modeling

| | |
|---|---|
| [**rctruta.github.io**](https://github.com/rctruta/rctruta.github.io) | The repository powering this website is built as a data modeling project. [→](https://ramonactruta.com/work.html#site-infrastructure) |

#### Benchmarking

| | |
|---|---|
| [**lakehouse-semantics**](https://github.com/rctruta/lakehouse-semantics) | A suite of 23 correctness probes executed across DuckDB, DuckDB+Delta, PostgreSQL, and Databricks SQL. [→](https://ramonactruta.com/work.html#lakehouse-semantics) |

#### AI evaluation

| | |
|---|---|
| [**harness-bench**](https://github.com/rctruta/harness-bench) | I engineered **harness-bench** to evaluate agent deployments before they reach production. [→](https://ramonactruta.com/work.html#harness-bench) |
| [**malloy-publisher-agent-study**](https://github.com/rctruta/malloy-publisher-agent-study) | The Malloy Publisher ships agent skills alongside its MCP server. [→](https://ramonactruta.com/work.html#malloy-study) |
| [**bauplan-agent-parse-study**](https://github.com/rctruta/bauplan-agent-parse-study) | Per-turn agent traces against a commercial lakehouse platform. Surfaced three defects I reported upstream — #369, #370, #371 — including an error message that actively sends an agent in the wrong direction. [→](https://ramonactruta.com/work.html#agent-traces) |
| [**agent-telemetry**](https://github.com/rctruta/agent-telemetry) | A local analytics package that parses raw JSONL session transcripts from coding agents (Claude Code) into un-opinionated process metrics: `tool_calls_per_turn`, `reads_before_first_edit`, `repeated_commands`, `error_rate`, `seconds_to_first_write`, and `edit_revisits`. [→](https://ramonactruta.com/work.html#agent-telemetry) |
| [**podcast-rag**](https://github.com/rctruta/podcast-rag) | Ask a question about a podcast, get an answer and a link to the exact second someone said it. LanceDB, local-first, no cluster and no API key. Built a labelled eval set and found it answering 17 of 20 questions its sources couldn't support; recalibrated precision 0.56 → 0.87. [→](https://ramonactruta.com/work.html#rag-accuracy) |
| [**music_recommendation_system**](https://github.com/rctruta/music_recommendation_system) | Top-10 song recommendation over the Million Song Dataset Taste Profile Subset: two million listening events, ten thousand songs. [→](https://ramonactruta.com/work.html#music-recommender) |

#### AI security

| | |
|---|---|
| [**adversarial-judgement-research**](https://github.com/rctruta/adversarial-judgement-research) | Metatracing engine and execution traces for structural failure modes in multi-agent LLM consensus pipelines: status bias, persona bleed, frame break, axiomatic refusal, consensus contagion, semantic camouflage. [→](https://ramonactruta.com/work.html#consensus-contagion) |
| [**ai-agent-utils**](https://github.com/rctruta/ai-agent-utils) | Boilerplate and security guidelines for collaborating safely with autonomous coding agents, with the gates already enforced rather than written down and hoped for. [→](https://ramonactruta.com/work.html#agent-tools) |

---

### Writing

- [A README is a Set of Falsifiable Claims](https://ramonactruta.substack.com/p/a-readme-is-a-set-of-falsifiable) — Testing mine found a security command that never worked.
- [Measuring Quack: DuckDB's New Client-Server Protocol](https://ramonactruta.substack.com/p/measuring-quack-duckdbs-new-client) — Pushdown holds a bounded ~2x overhead and beats PostgreSQL on analytical aggregations; attach mode does not scale, and cannot join at all.
- [The Job That Wasn't](https://ramonactruta.substack.com/p/the-job-that-wasnt-how-ai-companies) — When you apply for a gig job in AI, you might be the product — not the candidate.
- [The Emotional P&L](https://ramonactruta.substack.com/p/the-emotional-p-and-l-why-we-pay) — Why we pay compounding interest on unexamined feelings.
- [Context is Empathy: The Cognitive Firewalls We Build Under Pressure](https://ramonactruta.substack.com/p/context-is-empathy-the-cognitive) — Why ignoring structural vulnerabilities in AI isn't ignorance — it's a survival mechanism.

[Everything →](https://ramonactruta.com/writing.html)

### Speaking

- **Neo4j NODES** — *Structure Is Not Security: Poisoning Graph-Based Agent Memory Through the Extraction Pipeline* · virtual · November 12, 2026
- **Data in the D** — *Measure What Matters* · Detroit · October 16, 2026
- **Canadian Women in Cybersecurity** — *Consensus Contagion: Status Bias and the RLHF Tax in Agentic AI Routing Nodes* · Toronto · May 26, 2026
- **AI Tinkerers Toronto** — *Semantic Laundering: Agentic Memory* · Toronto · February 26, 2026

[Everything →](https://ramonactruta.com/speaking.html)

<!-- Generated by tools/build_github_readme.py in rctruta/rctruta.github.io,
     from the same data as the website. Edit the data, not this file. -->
