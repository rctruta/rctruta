<!-- The curated block at the top of README.md.
     Everything else in that file is generated from the website's data by
     tools/build_github_readme.py in rctruta.github.io. This part is written by
     hand because it is a pitch, not a record — the numbers in it are capsule
     findings registered in FACTS.yaml.
     featured-repo: https://github.com/rctruta/sql-benchmarks-dagster -->

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
