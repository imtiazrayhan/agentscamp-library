# Commands

> Reusable slash commands that automate repeatable workflows in Claude Code.

Install any of these with the [`agentscamp`](https://www.npmjs.com/package/agentscamp) CLI (`-g` installs to `~/.claude/` instead of the current project), or open the linked file and copy it into your `.claude/commands/` directory. Each entry links to its full page on [AgentsCamp](https://agentscamp.com).

**29 commands** · [← Back to README](README.md)

## Review

- **[Benchmark Rerankers](commands/benchmark-rerankers.md)** — Measure whether adding a reranker actually improves retrieval, by scoring reranked vs. un-reranked results on a labeled query set.
  [↗ Page](https://agentscamp.com/commands/review/benchmark-rerankers) · `npx agentscamp add commands/benchmark-rerankers`
- **[Find Bug](commands/find-bug.md)** — Investigate a reported symptom, form hypotheses, and locate the root cause.
  [↗ Page](https://agentscamp.com/commands/review/find-bug) · `npx agentscamp add commands/find-bug`
- **[Red Team LLM](commands/red-team-llm.md)** — Red-team an LLM app or agent for prompt injection, jailbreaks, and data leakage — probe the real attack surface (input, RAG, tools, system prompt) with adversarial inputs and report what got through and how to fix it.
  [↗ Page](https://agentscamp.com/commands/review/red-team-llm) · `npx agentscamp add commands/red-team-llm`
- **[Review PR](commands/review-pr.md)** — Review a pull request for correctness, security, and style, and summarize findings.
  [↗ Page](https://agentscamp.com/commands/review/review-pr) · `npx agentscamp add commands/review-pr`
- **[Security Scan](commands/security-scan.md)** — Scan the current diff or given paths for security vulnerabilities.
  [↗ Page](https://agentscamp.com/commands/review/security-scan) · `npx agentscamp add commands/security-scan`

## Scaffold

- **[Add Human Approval Step](commands/add-human-approval.md)** — Scaffold a human-in-the-loop approval gate into an agent so it pauses before a consequential action and resumes after approval.
  [↗ Page](https://agentscamp.com/commands/scaffold/add-human-approval) · `npx agentscamp add commands/add-human-approval`
- **[Add a Streaming LLM Endpoint](commands/add-streaming-endpoint.md)** — Scaffold a token-streaming LLM endpoint — server-side streaming plus the client handler — so responses render incrementally instead of after a long wait.
  [↗ Page](https://agentscamp.com/commands/scaffold/add-streaming-endpoint) · `npx agentscamp add commands/add-streaming-endpoint`
- **[New Component](commands/new-component.md)** — Scaffold a new UI component matching the project conventions.
  [↗ Page](https://agentscamp.com/commands/scaffold/new-component) · `npx agentscamp add commands/new-component`
- **[Scaffold a vLLM Serving Config](commands/scaffold-vllm-config.md)** — Scaffold a vLLM serving config for a model on a target GPU — pick precision/quantization and parallelism to fit, set batching and context length, and expose an OpenAI-compatible server.
  [↗ Page](https://agentscamp.com/commands/scaffold/scaffold-vllm-config) · `npx agentscamp add commands/scaffold-vllm-config`

## Docs

- **[Add Docstrings](commands/add-docstrings.md)** — Add or improve docstrings for the public API of a file or symbol.
  [↗ Page](https://agentscamp.com/commands/docs/add-docstrings) · `npx agentscamp add commands/add-docstrings`
- **[Explain Code](commands/explain-code.md)** — Explain what the given code does, in clear prose with a short summary.
  [↗ Page](https://agentscamp.com/commands/docs/explain-code) · `npx agentscamp add commands/explain-code`
- **[Update README](commands/update-readme.md)** — Update the README to reflect the current scripts, structure, and features of the repo.
  [↗ Page](https://agentscamp.com/commands/docs/update-readme) · `npx agentscamp add commands/update-readme`

## Git

- **[Commit](commands/commit.md)** — Stage changes and write a Conventional Commits message describing them.
  [↗ Page](https://agentscamp.com/commands/git/commit) · `npx agentscamp add commands/commit`
- **[Create PR](commands/create-pr.md)** — Push the current branch and open a GitHub pull request with a generated title and body.
  [↗ Page](https://agentscamp.com/commands/git/create-pr) · `npx agentscamp add commands/create-pr`
- **[Sync Branch](commands/sync-branch.md)** — Fetch and rebase the current branch onto its base, resolving conflicts and verifying the build.
  [↗ Page](https://agentscamp.com/commands/git/sync-branch) · `npx agentscamp add commands/sync-branch`

## Testing

- **[Fix Failing Test](commands/fix-failing-test.md)** — Diagnose and fix a failing test by finding the real root cause.
  [↗ Page](https://agentscamp.com/commands/testing/fix-failing-test) · `npx agentscamp add commands/fix-failing-test`
- **[Run Evals](commands/run-evals.md)** — Run the project's LLM evaluation suite (DeepEval, promptfoo, or RAGAS) and report scores against thresholds before a merge.
  [↗ Page](https://agentscamp.com/commands/testing/run-evals) · `npx agentscamp add commands/run-evals`
- **[Write Tests](commands/write-tests.md)** — Generate tests covering the happy path and edge cases for the given target.
  [↗ Page](https://agentscamp.com/commands/testing/write-tests) · `npx agentscamp add commands/write-tests`

## Db

- **[DB Migrate](commands/db-migrate.md)** — Generate and apply a database migration the safe way — using the project's migration tool, with expand-contract discipline for breaking changes, lock-free DDL, and a reversible up/down.
  [↗ Page](https://agentscamp.com/commands/db/db-migrate) · `npx agentscamp add commands/db-migrate`
- **[Scaffold a pgvector Schema & HNSW Index](commands/scaffold-pgvector-schema.md)** — Scaffold a production-ready pgvector schema and HNSW index for a corpus — matching the project's migration tooling, distance metric, and embedding dimensions.
  [↗ Page](https://agentscamp.com/commands/db/scaffold-pgvector-schema) · `npx agentscamp add commands/scaffold-pgvector-schema`

## Perf

- **[Profile Postgres Queries](commands/profile-postgres-queries.md)** — Profile a Postgres workload to find the queries actually costing you — rank by total time with pg_stat_statements, EXPLAIN the worst offenders, and recommend the highest-leverage fix.
  [↗ Page](https://agentscamp.com/commands/perf/profile-postgres-queries) · `npx agentscamp add commands/profile-postgres-queries`
- **[Set Perf Budget](commands/set-perf-budget.md)** — Define and enforce a cost and latency budget for an LLM feature or endpoint — set p95/p99 latency and cost-per-request ceilings, instrument to measure them against real traffic, and wire a check that fails when the budget is breached.
  [↗ Page](https://agentscamp.com/commands/perf/set-perf-budget) · `npx agentscamp add commands/set-perf-budget`

## Plan

- **[Breakdown Task](commands/breakdown-task.md)** — Decompose a task into an ordered checklist of small, verifiable steps.
  [↗ Page](https://agentscamp.com/commands/plan/breakdown-task) · `npx agentscamp add commands/breakdown-task`
- **[Plan Feature](commands/plan-feature.md)** — Explore the codebase and produce an implementation plan for a feature.
  [↗ Page](https://agentscamp.com/commands/plan/plan-feature) · `npx agentscamp add commands/plan-feature`

## Refactor

- **[Extract Function](commands/extract-function.md)** — Extract a code region into a well-named function and update the call site.
  [↗ Page](https://agentscamp.com/commands/refactor/extract-function) · `npx agentscamp add commands/extract-function`
- **[Refactor](commands/refactor.md)** — Refactor the target for readability and structure without changing behavior.
  [↗ Page](https://agentscamp.com/commands/refactor/refactor) · `npx agentscamp add commands/refactor`

## Workflow

- **[Add MCP Server](commands/add-mcp-server.md)** — Add an MCP server to the current project the safe way — pick the transport and scope, wire secrets through env vars, vet provenance, and verify the connection before trusting it.
  [↗ Page](https://agentscamp.com/commands/workflow/add-mcp-server) · `npx agentscamp add commands/add-mcp-server`
- **[Setup Claude CI](commands/setup-claude-ci.md)** — Wire Claude Code into this repo's CI the safe way — install the GitHub App or scaffold the workflow YAML, scope permissions to the minimum, set secrets correctly, and verify with a real trigger.
  [↗ Page](https://agentscamp.com/commands/workflow/setup-claude-ci) · `npx agentscamp add commands/setup-claude-ci`

## Analyze

- **[Explain Error](commands/explain-error.md)** — Diagnose an error message or stack trace and propose a fix.
  [↗ Page](https://agentscamp.com/commands/analyze/explain-error) · `npx agentscamp add commands/explain-error`
