### Ramona C. Truta

I build the instruments that measure whether database and AI agent systems actually do what
they claim — then publish the experiment alongside the result, so you can reproduce it or show
me where I'm wrong.

[Portfolio](https://rctruta.github.io) · [Writing](https://ramonactruta.substack.com) · [LinkedIn](https://linkedin.com/in/ramonactruta) · [ORCID](https://orcid.org/0009-0008-4886-7777)

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

#### Agents, measured the same way

I study AI agent systems by instrumenting them and reading the traces.

| | |
|---|---|
| [**bauplan-agent-parse-study**](https://github.com/rctruta/bauplan-agent-parse-study) | Per-turn agent traces against a commercial lakehouse platform. Surfaced three defects I reported upstream — [#369](https://github.com/BauplanLabs/bauplan/issues/369), [#370](https://github.com/BauplanLabs/bauplan/issues/370), [#371](https://github.com/BauplanLabs/bauplan/issues/371) — including an error message that actively sends an agent in the wrong direction. |
| [**podcast-rag**](https://github.com/rctruta/podcast-rag) | Ask a question about a podcast, get an answer and a link to the exact second someone said it. LanceDB, local-first, no cluster and no API key. Built a labelled eval set and found it answering 17 of 20 questions its sources couldn't support; recalibrated precision 0.56 → 0.87. |
| [**ai-agent-utils**](https://github.com/rctruta/ai-agent-utils) | Boilerplate and security guidelines for collaborating safely with autonomous coding agents. |
| [**awesome-pedantic-medallion**](https://github.com/rctruta/awesome-pedantic-medallion) | Community-curated playbooks for building shared understanding. |

---

#### Writing

- [Measuring Quack: DuckDB's New Client-Server Protocol](https://ramonactruta.substack.com/p/measuring-quack-duckdbs-new-client) — independent measurements of a protocol at beta, every number capsule-backed
- [The Blackboard and the Library](https://ramonactruta.substack.com/p/the-blackboard-and-the-library) — agents need two kinds of memory: the blackboard you erase, and the library that persists
- [A `README` is a Set of Falsifiable Claims](https://ramonactruta.substack.com/p/a-readme-is-a-set-of-falsifiable) — if your README says it works, that's a claim, and claims can be tested
- [Inside `~/.claude/`: Structure is Not Security](https://ramonactruta.substack.com/p/inside-claude-structure-is-not-security) — what a coding agent writes to your disk, in plaintext
- [The "Blueberry Muffin Exploit"](https://ramonactruta.substack.com/p/the-blueberry-muffin-exploit-semantic) — semantic injection into agent memory, disclosed

#### Speaking

- **Neo4j NODES 2026** — *Structure Is Not Security: Poisoning Graph-Based Agent Memory Through the Extraction Pipeline* · Nov 12, 2026
- **Data in the D 2026** — *Measure What Matters* · Detroit, Oct 16–17, 2026
- **Canadian Women in Cybersecurity 2026** — *Consensus Contagion: Status Bias and the RLHF Tax in Agentic AI Routing Nodes* · Toronto, May 26, 2026
- **Neo4j NODES 2025** — *Is My Brain a Knowledge Graph?* · Nov 6, 2025
