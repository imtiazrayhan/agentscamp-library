# Commands

> Reusable slash commands that automate repeatable workflows in Claude Code.

Install any of these with the [`agentscamp`](https://www.npmjs.com/package/agentscamp) CLI (`-g` installs to `~/.claude/` instead of the current project), or open the linked file and copy it into your `.claude/commands/` directory. Each entry links to its full page on [AgentsCamp](https://agentscamp.com).

**50 commands** · [← Back to README](README.md)

## Scaffold

- **[Add Human Approval Step](commands/add-human-approval.md)** — Scaffold a human-in-the-loop approval gate into an agent so it pauses before a consequential action and resumes after approval.
  [↗ Page](https://agentscamp.com/commands/scaffold/add-human-approval) · `npx agentscamp add commands/add-human-approval`
- **[Add a Streaming LLM Endpoint](commands/add-streaming-endpoint.md)** — Scaffold a token-streaming LLM endpoint — server-side streaming plus the client handler — so responses render incrementally instead of after a long wait.
  [↗ Page](https://agentscamp.com/commands/scaffold/add-streaming-endpoint) · `npx agentscamp add commands/add-streaming-endpoint`
- **[New Component](commands/new-component.md)** — Scaffold a new UI component matching the project conventions.
  [↗ Page](https://agentscamp.com/commands/scaffold/new-component) · `npx agentscamp add commands/new-component`
- **[Scaffold Dockerfile](commands/scaffold-dockerfile.md)** — Scaffold a production-grade multi-stage Dockerfile and .dockerignore for the current project.
  [↗ Page](https://agentscamp.com/commands/scaffold/scaffold-dockerfile) · `npx agentscamp add commands/scaffold-dockerfile`
- **[Scaffold GitHub Action](commands/scaffold-github-action.md)** — Scaffold a hardened GitHub Actions workflow for a stated goal, wired to the project's real test/lint/build commands.
  [↗ Page](https://agentscamp.com/commands/scaffold/scaffold-github-action) · `npx agentscamp add commands/scaffold-github-action`
- **[Scaffold RAG Pipeline](commands/scaffold-rag-pipeline.md)** — Scaffold a Retrieval-Augmented Generation pipeline — ingestion (load, chunk, embed, upsert) and retrieval (search, rerank, grounded prompt with citations) — fitted to the project's stack.
  [↗ Page](https://agentscamp.com/commands/scaffold/scaffold-rag-pipeline) · `npx agentscamp add commands/scaffold-rag-pipeline`
- **[Scaffold a vLLM Serving Config](commands/scaffold-vllm-config.md)** — Scaffold a vLLM serving config for a model on a target GPU — pick precision/quantization and parallelism to fit, set batching and context length, and expose an OpenAI-compatible server.
  [↗ Page](https://agentscamp.com/commands/scaffold/scaffold-vllm-config) · `npx agentscamp add commands/scaffold-vllm-config`

## Git

- **[Clean Branches](commands/clean-branches.md)** — Safely prune merged and stale Git branches: drop dead remote-tracking refs, list merged candidates for review, then delete with the safe -d variant.
  [↗ Page](https://agentscamp.com/commands/git/clean-branches) · `npx agentscamp add commands/clean-branches`
- **[Commit](commands/commit.md)** — Stage changes and write a Conventional Commits message describing them.
  [↗ Page](https://agentscamp.com/commands/git/commit) · `npx agentscamp add commands/commit`
- **[Create PR](commands/create-pr.md)** — Push the current branch and open a GitHub pull request with a generated title and body.
  [↗ Page](https://agentscamp.com/commands/git/create-pr) · `npx agentscamp add commands/create-pr`
- **[Git Bisect](commands/git-bisect.md)** — Drive git bisect to find the exact commit that introduced a regression.
  [↗ Page](https://agentscamp.com/commands/git/git-bisect) · `npx agentscamp add commands/git-bisect`
- **[Resolve Merge Conflicts](commands/resolve-conflict.md)** — Walk through resolving the in-progress merge, rebase, or cherry-pick conflict in the current repo by understanding both sides, then verify before continuing.
  [↗ Page](https://agentscamp.com/commands/git/resolve-conflict) · `npx agentscamp add commands/resolve-conflict`
- **[Sync Branch](commands/sync-branch.md)** — Fetch and rebase the current branch onto its base, resolving conflicts and verifying the build.
  [↗ Page](https://agentscamp.com/commands/git/sync-branch) · `npx agentscamp add commands/sync-branch`

## Review

- **[Benchmark Rerankers](commands/benchmark-rerankers.md)** — Measure whether adding a reranker actually improves retrieval, by scoring reranked vs. un-reranked results on a labeled query set.
  [↗ Page](https://agentscamp.com/commands/review/benchmark-rerankers) · `npx agentscamp add commands/benchmark-rerankers`
- **[Find Bug](commands/find-bug.md)** — Investigate a reported symptom, form hypotheses, and locate the root cause.
  [↗ Page](https://agentscamp.com/commands/review/find-bug) · `npx agentscamp add commands/find-bug`
- **[Red Team LLM](commands/red-team-llm.md)** — Red-team an LLM app or agent for prompt injection, jailbreaks, and data leakage — probe the real attack surface (input, RAG, tools, system prompt) with adversarial inputs and report what got through and how to fix it.
  [↗ Page](https://agentscamp.com/commands/review/red-team-llm) · `npx agentscamp add commands/red-team-llm`
- **[Review PR](commands/review-pr.md)** — Review a pull request for correctness, security, and style, and summarize findings.
  [↗ Page](https://agentscamp.com/commands/review/review-pr) · `npx agentscamp add commands/review-pr`
- **[Review Tests](commands/review-tests.md)** — Review the quality of a test suite, not just whether it passes — find weak assertions, missing edge cases, and tests coupled to implementation.
  [↗ Page](https://agentscamp.com/commands/review/review-tests) · `npx agentscamp add commands/review-tests`
- **[Security Scan](commands/security-scan.md)** — Scan the current diff or given paths for security vulnerabilities.
  [↗ Page](https://agentscamp.com/commands/review/security-scan) · `npx agentscamp add commands/security-scan`

## Workflow

- **[Add MCP Server](commands/add-mcp-server.md)** — Add an MCP server to the current project the safe way — pick the transport and scope, wire secrets through env vars, vet provenance, and verify the connection before trusting it.
  [↗ Page](https://agentscamp.com/commands/workflow/add-mcp-server) · `npx agentscamp add commands/add-mcp-server`
- **[Create Skill](commands/create-skill.md)** — Scaffold a new Claude Code skill into .claude/skills/<name>/SKILL.md — a model-invoked capability with a trigger-rich description, scoped tools, and a lean body that pushes detail into resource files.
  [↗ Page](https://agentscamp.com/commands/workflow/create-skill) · `npx agentscamp add commands/create-skill`
- **[Create Slash Command](commands/create-slash-command.md)** — Scaffold a new Claude Code slash command into .claude/commands/ — a valid Markdown file with frontmatter, a least-privilege allowed-tools allowlist, and a $ARGUMENTS-driven body of numbered steps ending in a Report.
  [↗ Page](https://agentscamp.com/commands/workflow/create-slash-command) · `npx agentscamp add commands/create-slash-command`
- **[Create Subagent](commands/create-subagent.md)** — Scaffold a new Claude Code subagent definition file into .claude/agents/ with a routing-ready description, scoped tools, and a system prompt.
  [↗ Page](https://agentscamp.com/commands/workflow/create-subagent) · `npx agentscamp add commands/create-subagent`
- **[Setup Claude CI](commands/setup-claude-ci.md)** — Wire Claude Code into this repo's CI the safe way — install the GitHub App or scaffold the workflow YAML, scope permissions to the minimum, set secrets correctly, and verify with a real trigger.
  [↗ Page](https://agentscamp.com/commands/workflow/setup-claude-ci) · `npx agentscamp add commands/setup-claude-ci`
- **[Setup Pre-commit Hooks](commands/setup-precommit-hooks.md)** — Set up fast pre-commit hooks that catch problems before they land — detect the repo's existing stack and hook mechanism, run lint/format/typecheck plus a secret scan on staged files only, keep the slow test suite in CI, and make the setup reproducible for the whole team.
  [↗ Page](https://agentscamp.com/commands/workflow/setup-precommit-hooks) · `npx agentscamp add commands/setup-precommit-hooks`

## Testing

- **[Fix Failing Test](commands/fix-failing-test.md)** — Diagnose and fix a failing test by finding the real root cause.
  [↗ Page](https://agentscamp.com/commands/testing/fix-failing-test) · `npx agentscamp add commands/fix-failing-test`
- **[Hunt Flaky Tests](commands/flaky-test-hunt.md)** — Reproduce a flaky test, find the real source of nondeterminism, and fix the cause.
  [↗ Page](https://agentscamp.com/commands/testing/flaky-test-hunt) · `npx agentscamp add commands/flaky-test-hunt`
- **[Generate E2E Test](commands/generate-e2e-test.md)** — Scaffold a resilient end-to-end test for a user flow grounded in the real UI.
  [↗ Page](https://agentscamp.com/commands/testing/generate-e2e-test) · `npx agentscamp add commands/generate-e2e-test`
- **[Run Evals](commands/run-evals.md)** — Run the project's LLM evaluation suite (DeepEval, promptfoo, or RAGAS) and report scores against thresholds before a merge.
  [↗ Page](https://agentscamp.com/commands/testing/run-evals) · `npx agentscamp add commands/run-evals`
- **[Write Tests](commands/write-tests.md)** — Generate tests covering the happy path and edge cases for the given target.
  [↗ Page](https://agentscamp.com/commands/testing/write-tests) · `npx agentscamp add commands/write-tests`

## Perf

- **[Add Caching](commands/add-caching.md)** — Add a caching layer to one expensive function or endpoint correctly — confirm it's cacheable, design the cache key/TTL/layer/invalidation, handle stampedes, wrap the call in one place, and report the design.
  [↗ Page](https://agentscamp.com/commands/perf/add-caching) · `npx agentscamp add commands/add-caching`
- **[Find N+1 Queries](commands/find-n-plus-one.md)** — Scan code read-only for N+1 query patterns — loops that query per iteration and handlers that fan out per-row — and report each with a location, why it is N+1, and the concrete eager-load/batch/set-based fix.
  [↗ Page](https://agentscamp.com/commands/perf/find-n-plus-one) · `npx agentscamp add commands/find-n-plus-one`
- **[Profile Postgres Queries](commands/profile-postgres-queries.md)** — Profile a Postgres workload to find the queries actually costing you — rank by total time with pg_stat_statements, EXPLAIN the worst offenders, and recommend the highest-leverage fix.
  [↗ Page](https://agentscamp.com/commands/perf/profile-postgres-queries) · `npx agentscamp add commands/profile-postgres-queries`
- **[Set Perf Budget](commands/set-perf-budget.md)** — Define and enforce a cost and latency budget for an LLM feature or endpoint — set p95/p99 latency and cost-per-request ceilings, instrument to measure them against real traffic, and wire a check that fails when the budget is breached.
  [↗ Page](https://agentscamp.com/commands/perf/set-perf-budget) · `npx agentscamp add commands/set-perf-budget`

## Plan

- **[Breakdown Task](commands/breakdown-task.md)** — Decompose a task into an ordered checklist of small, verifiable steps.
  [↗ Page](https://agentscamp.com/commands/plan/breakdown-task) · `npx agentscamp add commands/breakdown-task`
- **[Estimate Effort](commands/estimate-effort.md)** — Produce a grounded effort and complexity estimate for a task by exploring the codebase read-only.
  [↗ Page](https://agentscamp.com/commands/plan/estimate-effort) · `npx agentscamp add commands/estimate-effort`
- **[Plan Feature](commands/plan-feature.md)** — Explore the codebase and produce an implementation plan for a feature.
  [↗ Page](https://agentscamp.com/commands/plan/plan-feature) · `npx agentscamp add commands/plan-feature`
- **[Write Design Doc](commands/write-design-doc.md)** — Explore the codebase and write a decision-oriented design doc / RFC for a feature or system change.
  [↗ Page](https://agentscamp.com/commands/plan/write-design-doc) · `npx agentscamp add commands/write-design-doc`

## Analyze

- **[Audit Accessibility](commands/audit-accessibility.md)** — Audit a component or page for accessibility against WCAG — semantics, names, keyboard, ARIA, contrast, forms, motion.
  [↗ Page](https://agentscamp.com/commands/analyze/audit-accessibility) · `npx agentscamp add commands/audit-accessibility`
- **[Explain Error](commands/explain-error.md)** — Diagnose an error message or stack trace and propose a fix.
  [↗ Page](https://agentscamp.com/commands/analyze/explain-error) · `npx agentscamp add commands/explain-error`
- **[Trace Data Flow](commands/trace-data-flow.md)** — Trace how a value, field, or variable flows through the codebase from source to sink.
  [↗ Page](https://agentscamp.com/commands/analyze/trace-data-flow) · `npx agentscamp add commands/trace-data-flow`

## Db

- **[DB Migrate](commands/db-migrate.md)** — Generate and apply a database migration the safe way — using the project's migration tool, with expand-contract discipline for breaking changes, lock-free DDL, and a reversible up/down.
  [↗ Page](https://agentscamp.com/commands/db/db-migrate) · `npx agentscamp add commands/db-migrate`
- **[Scaffold a pgvector Schema & HNSW Index](commands/scaffold-pgvector-schema.md)** — Scaffold a production-ready pgvector schema and HNSW index for a corpus — matching the project's migration tooling, distance metric, and embedding dimensions.
  [↗ Page](https://agentscamp.com/commands/db/scaffold-pgvector-schema) · `npx agentscamp add commands/scaffold-pgvector-schema`
- **[Seed Data](commands/seed-data.md)** — Generate realistic, referentially-consistent seed data and a re-runnable seed script from your actual schema — types and constraints respected, plausible values, FK-dependency insert order, idempotent, never aimed at production.
  [↗ Page](https://agentscamp.com/commands/db/seed-data) · `npx agentscamp add commands/seed-data`

## Docs

- **[Add Docstrings](commands/add-docstrings.md)** — Add or improve docstrings for the public API of a file or symbol.
  [↗ Page](https://agentscamp.com/commands/docs/add-docstrings) · `npx agentscamp add commands/add-docstrings`
- **[Explain Code](commands/explain-code.md)** — Explain what the given code does, in clear prose with a short summary.
  [↗ Page](https://agentscamp.com/commands/docs/explain-code) · `npx agentscamp add commands/explain-code`
- **[Update README](commands/update-readme.md)** — Update the README to reflect the current scripts, structure, and features of the repo.
  [↗ Page](https://agentscamp.com/commands/docs/update-readme) · `npx agentscamp add commands/update-readme`

## Refactor

- **[Extract Function](commands/extract-function.md)** — Extract a code region into a well-named function and update the call site.
  [↗ Page](https://agentscamp.com/commands/refactor/extract-function) · `npx agentscamp add commands/extract-function`
- **[Refactor](commands/refactor.md)** — Refactor the target for readability and structure without changing behavior.
  [↗ Page](https://agentscamp.com/commands/refactor/refactor) · `npx agentscamp add commands/refactor`
- **[Rename Symbol](commands/rename-symbol.md)** — Safely rename a symbol project-wide, distinguishing the real symbol from coincidental substring matches.
  [↗ Page](https://agentscamp.com/commands/refactor/rename-symbol) · `npx agentscamp add commands/rename-symbol`
