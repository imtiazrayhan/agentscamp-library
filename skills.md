# Skills

> Packaged SKILL.md capabilities that extend Claude with on-demand expertise.

Install any of these with the [`agentscamp`](https://www.npmjs.com/package/agentscamp) CLI (`-g` installs to `~/.claude/` instead of the current project), or open the linked file and copy it into your `.claude/skills/` directory. Each entry links to its full page on [AgentsCamp](https://agentscamp.com).

**38 skills** · [← Back to README](README.md)

## Data

- **[Chunking Strategy Optimizer](skills/chunking-strategy-optimizer/SKILL.md)** — Find the chunking strategy and size that maximizes retrieval quality for a specific corpus, by sweeping configurations against a fixed eval set instead of guessing. Use when RAG answers miss obvious content, when standing up a new corpus, or when picking chunk size/overlap.
  [↗ Page](https://agentscamp.com/skills/data/chunking-strategy-optimizer) · `npx agentscamp add skills/chunking-strategy-optimizer`
- **[Embedding Set Inspector](skills/embedding-set-inspector/SKILL.md)** — Diagnose the health of an embedding set before blaming the retriever — checking normalization, dimensionality, near-duplicates, degenerate vectors, and corpus/query distribution mismatch. Use when retrieval quality is poor, after a re-embed, or before shipping a new index.
  [↗ Page](https://agentscamp.com/skills/data/embedding-set-inspector) · `npx agentscamp add skills/embedding-set-inspector`
- **[Finetune Dataset Builder](skills/finetune-dataset-builder/SKILL.md)** — Turn raw examples into a training-ready fine-tuning dataset — normalize to the trainer's chat/instruction format, deduplicate (including near-duplicates), strip PII, balance, validate the schema and token lengths, and carve a leak-free eval split. Use when you have raw examples and need a clean, formatted, split dataset before training.
  [↗ Page](https://agentscamp.com/skills/data/finetune-dataset-builder) · `npx agentscamp add skills/finetune-dataset-builder`
- **[Graphrag Scaffolder](skills/graphrag-scaffolder/SKILL.md)** — Stand up a GraphRAG experiment the disciplined way: audit whether your failed queries are actually connection-shaped, scope a minimal entity/relationship ontology, build extraction → graph → community-summary indexing on a corpus slice, and measure against vector-RAG baselines before committing. Use when multi-hop or whole-corpus questions keep failing plain RAG.
  [↗ Page](https://agentscamp.com/skills/data/graphrag-scaffolder) · `npx agentscamp add skills/graphrag-scaffolder`
- **[LLM As Judge Scorer](skills/llm-as-judge-scorer/SKILL.md)** — Design a reliable LLM-as-judge metric — a calibrated rubric, a clear scoring scale, and bias controls — and validate it against human labels before trusting it. Use when grading open-ended LLM output (summaries, answers, tone) that exact-match can't score.
  [↗ Page](https://agentscamp.com/skills/data/llm-as-judge-scorer) · `npx agentscamp add skills/llm-as-judge-scorer`
- **[LLM Eval Suite Scaffolder](skills/llm-eval-suite-scaffolder/SKILL.md)** — Stand up an evaluation suite for an LLM feature from scratch — a representative dataset, the right metrics, a baseline score, and a CI gate — using DeepEval, promptfoo, or RAGAS. Use when a feature has no evals, before tuning a prompt, or when adding an LLM feature to CI.
  [↗ Page](https://agentscamp.com/skills/data/llm-eval-suite-scaffolder) · `npx agentscamp add skills/llm-eval-suite-scaffolder`
- **[Multimodal Document Extractor](skills/multimodal-document-extractor/SKILL.md)** — Extract structured data from documents and images with a vision-language model — define the target schema, prompt the VLM to fill it from the page (invoices, forms, receipts, statements, IDs), and verify critical fields against the source. Use when you need reliable structured output from messy, varied, or scanned documents that defeat template-based OCR.
  [↗ Page](https://agentscamp.com/skills/data/multimodal-document-extractor) · `npx agentscamp add skills/multimodal-document-extractor`
- **[Qlora Finetune Runner](skills/qlora-finetune-runner/SKILL.md)** — Run a QLoRA (4-bit LoRA) fine-tune of an open-weight model from a prepared dataset — set up the config, train memory-efficiently (e.g. with Unsloth/PEFT), watch for overfitting, save the adapter, and run a quick eval against the prepared split. Use when you have a clean dataset and want to execute a parameter-efficient fine-tune on a single GPU.
  [↗ Page](https://agentscamp.com/skills/data/qlora-finetune-runner) · `npx agentscamp add skills/qlora-finetune-runner`
- **[SQL Optimizer](skills/sql-optimizer/SKILL.md)** — Diagnose a slow SQL query from its execution plan and propose a verified optimization — finding the real bottleneck (sequential scan, missing or unused index, bad join order, app-side N+1) and measuring the fix before and after. Use when a query is slow and you need a fix backed by EXPLAIN ANALYZE, not a guess.
  [↗ Page](https://agentscamp.com/skills/data/sql-optimizer) · `npx agentscamp add skills/sql-optimizer`
- **[Web Research Pipeline](skills/web-research-pipeline/SKILL.md)** — Run a structured web-research pass on a question: plan the searches, find sources via search APIs, fetch and read the best ones, cross-check claims, and synthesize a cited answer — with source quality and disagreements surfaced honestly. Use for 'research X and tell me what's actually true' tasks that need more than one search and less than a day.
  [↗ Page](https://agentscamp.com/skills/data/web-research-pipeline) · `npx agentscamp add skills/web-research-pipeline`

## Workflow

- **[Claude Settings Auditor](skills/claude-settings-auditor/SKILL.md)** — Audit every Claude Code settings layer — user, project, local, and managed — and report the effective merged configuration with its risks: over-broad Bash allows, missing deny rules for secrets, bypassPermissions defaults, unvetted MCP servers and hooks, and rules that never match. Use before trusting a new repo's checked-in settings, or to harden your own before handing the agent more autonomy.
  [↗ Page](https://agentscamp.com/skills/workflow/claude-settings-auditor) · `npx agentscamp add skills/claude-settings-auditor`
- **[Hook Writer](skills/hook-writer/SKILL.md)** — Turn a plain-language automation request — 'format every file Claude edits', 'block writes to migrations', 'notify me when input is needed' — into a working Claude Code hook: the right event, a safe tested script, and the settings.json registration at the right scope. Use when you want a hook but don't want to hand-write the matcher, stdin JSON parsing, and exit-code plumbing.
  [↗ Page](https://agentscamp.com/skills/workflow/hook-writer) · `npx agentscamp add skills/hook-writer`
- **[Human In The Loop Gate](skills/human-in-the-loop-gate/SKILL.md)** — Add a human approval checkpoint to an agent so it pauses before a risky or irreversible action (spending money, deleting data, sending messages, merging code) and resumes only after a human approves. Use when an agent acts autonomously on consequential operations.
  [↗ Page](https://agentscamp.com/skills/workflow/human-in-the-loop-gate) · `npx agentscamp add skills/human-in-the-loop-gate`
- **[Plugin Scaffolder](skills/plugin-scaffolder/SKILL.md)** — Scaffold a complete, valid Claude Code plugin from a description — the .claude-plugin/plugin.json manifest, component directories (skills, agents, commands, hooks, MCP config), portable ${CLAUDE_PLUGIN_ROOT} wiring, a local test loop with --plugin-dir, and a marketplace.json for distribution. Use when turning scattered .claude/ customizations into one installable, versioned package.
  [↗ Page](https://agentscamp.com/skills/workflow/plugin-scaffolder) · `npx agentscamp add skills/plugin-scaffolder`
- **[Prompt Optimizer](skills/prompt-optimizer/SKILL.md)** — Diagnose why a prompt underperforms and rewrite it with the technique that fixes it — clearer structure, few-shot examples, an explicit output contract, or reasoning scaffolding — returning an optimized prompt, the rationale for every change, and what to measure to confirm the lift. Use when a prompt is flaky, verbose, drifting in format, or just not good enough.
  [↗ Page](https://agentscamp.com/skills/workflow/prompt-optimizer) · `npx agentscamp add skills/prompt-optimizer`

## API

- **[LLM Output Schema Generator](skills/llm-output-schema-generator/SKILL.md)** — Turn an example of the data you want from an LLM into a precise, validated output schema (Pydantic / Zod / JSON Schema) and wire it into structured-output calls. Use when adding typed LLM output, replacing brittle JSON parsing, or designing an extraction shape.
  [↗ Page](https://agentscamp.com/skills/api/llm-output-schema-generator) · `npx agentscamp add skills/llm-output-schema-generator`
- **[MCP Server Scaffolder](skills/mcp-server-scaffolder/SKILL.md)** — Scaffold a new Model Context Protocol (MCP) server from a description — pick the SDK and transport, generate a typed first tool with a strict schema, and wire up MCP Inspector testing and the client-registration command. Use when starting a new MCP server and you want a correct, runnable skeleton instead of copying a README.
  [↗ Page](https://agentscamp.com/skills/api/mcp-server-scaffolder) · `npx agentscamp add skills/mcp-server-scaffolder`
- **[Provider Fallback Wrapper](skills/provider-fallback-wrapper/SKILL.md)** — Wrap LLM calls so a provider outage, rate limit, or timeout degrades gracefully — with multi-provider fallback, bounded retries with backoff, and timeouts. Use when an app depends on a single model/provider and needs production resilience.
  [↗ Page](https://agentscamp.com/skills/api/provider-fallback-wrapper) · `npx agentscamp add skills/provider-fallback-wrapper`
- **[Tool Definition Generator](skills/tool-definition-generator/SKILL.md)** — Generate clean function/tool schemas for an LLM agent from existing code or a spec — accurate JSON Schema, model-facing descriptions, honest required fields, and enums that make invalid calls impossible. Use when wiring functions into an agent's tool-calling loop.
  [↗ Page](https://agentscamp.com/skills/api/tool-definition-generator) · `npx agentscamp add skills/tool-definition-generator`

## Security

- **[Dependency Audit](skills/dependency-audit/SKILL.md)** — Audit project dependencies for known vulnerabilities and turn the raw scanner output into a triaged, prioritized upgrade plan. Use when an audit is noisy, a CVE was reported, or you need to know which advisories actually matter.
  [↗ Page](https://agentscamp.com/skills/security/dependency-audit) · `npx agentscamp add skills/dependency-audit`
- **[LLM Guardrails Designer](skills/llm-guardrails-designer/SKILL.md)** — Design input and output guardrails for an LLM app — decide what to check (injection patterns, PII, secrets, policy, schema, leakage, toxicity), place them as input vs. output rails, implement with a library like NeMo Guardrails or LLM Guard, and fail closed. Use when adding a safety/validation layer around an LLM, not relying on the prompt alone.
  [↗ Page](https://agentscamp.com/skills/security/llm-guardrails-designer) · `npx agentscamp add skills/llm-guardrails-designer`
- **[Prompt Pii Redactor](skills/prompt-pii-redactor/SKILL.md)** — Detect and redact PII and secrets from prompts (and logs/traces) before they reach an LLM provider — mask or tokenize emails, phone numbers, names, IDs, and API keys, reversibly where the response needs the real values back. Use when sending user or document data to a third-party model, or when LLM request logs may capture sensitive data.
  [↗ Page](https://agentscamp.com/skills/security/prompt-pii-redactor) · `npx agentscamp add skills/prompt-pii-redactor`
- **[Secret Scanner](skills/secret-scanner/SKILL.md)** — Scan a repo or a diff for committed secrets — API keys, tokens, private keys, .env files, and high-entropy strings — then triage real leaks from fixtures. Use before pushing, in review, or when a credential may have leaked.
  [↗ Page](https://agentscamp.com/skills/security/secret-scanner) · `npx agentscamp add skills/secret-scanner`

## Docs

- **[Adr Writer](skills/adr-writer/SKILL.md)** — Write an Architecture Decision Record capturing a decision the user describes, in Michael Nygard ADR format (Status, Context, Decision, Consequences) with an added Considered Alternatives section. Use when recording a significant architectural or technology choice.
  [↗ Page](https://agentscamp.com/skills/docs/adr-writer) · `npx agentscamp add skills/adr-writer`
- **[OpenAPI Doc Writer](skills/openapi-doc-writer/SKILL.md)** — Produce and maintain OpenAPI documentation for an HTTP API. Use when documenting endpoints, request/response schemas, or generating API reference docs.
  [↗ Page](https://agentscamp.com/skills/docs/openapi-doc-writer) · `npx agentscamp add skills/openapi-doc-writer`
- **[Readme Generator](skills/readme-generator/SKILL.md)** — Generate or refresh a project README grounded in the actual repository. Use when a project has no README, a stale one, or you want install/usage/scripts/structure sections that match the real code.
  [↗ Page](https://agentscamp.com/skills/docs/readme-generator) · `npx agentscamp add skills/readme-generator`

## Git

- **[Branch Rebaser](skills/branch-rebaser/SKILL.md)** — Rebase the current branch onto its base and walk every conflict methodically, resolving each by understanding both sides. Use when your feature branch has fallen behind main and you want a clean, linear history without clobbering changes.
  [↗ Page](https://agentscamp.com/skills/git/branch-rebaser) · `npx agentscamp add skills/branch-rebaser`
- **[Conventional Commits](skills/conventional-commits/SKILL.md)** — Generate clear Conventional Commits messages from staged changes. Use when committing code and you want a well-structured, consistent commit message.
  [↗ Page](https://agentscamp.com/skills/git/conventional-commits) · `npx agentscamp add skills/conventional-commits`
- **[PR Description](skills/pr-description/SKILL.md)** — Draft a clear pull request description from the branch diff against its base. Use when you have a finished branch and want a reviewer-ready PR body before opening the PR.
  [↗ Page](https://agentscamp.com/skills/git/pr-description) · `npx agentscamp add skills/pr-description`

## Testing

- **[Coverage Gap Finder](skills/coverage-gap-finder/SKILL.md)** — Run the project's coverage tool and identify the highest-value untested paths — error branches, edge cases, and critical modules — then propose specific test cases for each gap. Use when you have a coverage report but don't know where new tests will pay off most.
  [↗ Page](https://agentscamp.com/skills/testing/coverage-gap-finder) · `npx agentscamp add skills/coverage-gap-finder`
- **[Mock Data Factory](skills/mock-data-factory/SKILL.md)** — Generate a typed mock/fixture factory for a given type, interface, or schema, inferring believable values from field names and types. Use when tests or local dev need realistic, type-safe sample data with per-field overrides.
  [↗ Page](https://agentscamp.com/skills/testing/mock-data-factory) · `npx agentscamp add skills/mock-data-factory`
- **[Test Scaffolder](skills/test-scaffolder/SKILL.md)** — Scaffold a test file with sensible cases for a given module or function. Use when adding tests to untested code and you want a fast, structured starting point.
  [↗ Page](https://agentscamp.com/skills/testing/test-scaffolder) · `npx agentscamp add skills/test-scaffolder`

## Database

- **[Embedding Index Tuner](skills/embedding-index-tuner/SKILL.md)** — Tune a vector index — HNSW graph parameters and quantization — to hit a recall target at the lowest latency and memory, by sweeping settings against a fixed query set instead of trusting defaults. Use when vector search is slow or memory-hungry, when recall dropped after enabling quantization, or when standing up an index and you need defensible parameters.
  [↗ Page](https://agentscamp.com/skills/database/embedding-index-tuner) · `npx agentscamp add skills/embedding-index-tuner`
- **[Postgres Index Strategist](skills/postgres-index-strategist/SKILL.md)** — Recommend the right Postgres index for a query or workload — choosing B-Tree vs. GIN vs. BRIN vs. partial/covering/expression, checking for redundant or unused indexes, and verifying the choice against the query plan. Use when a query needs an index, when deciding an index type for jsonb/array/full-text/time-series data, or when auditing an over-indexed table.
  [↗ Page](https://agentscamp.com/skills/database/postgres-index-strategist) · `npx agentscamp add skills/postgres-index-strategist`

## Performance

- **[Bundle Analyzer](skills/bundle-analyzer/SKILL.md)** — Analyze a JS/TS production bundle and surface the biggest size wins — heavy dependencies, duplicate packages, missing code-splitting, oversized polyfills, and dev/server code leaking into the client. Use when a bundle is too large and you need a ranked, actionable reduction plan.
  [↗ Page](https://agentscamp.com/skills/performance/bundle-analyzer) · `npx agentscamp add skills/bundle-analyzer`
- **[Prompt Cache Optimizer](skills/prompt-cache-optimizer/SKILL.md)** — Restructure an LLM call to maximize prompt-cache hit rate and add response/semantic caching — move the stable prefix (system prompt, instructions, few-shot, context) to the front and variable input to the end, set cache breakpoints, and measure the hit rate and savings. Use when repeated calls share large common context and token cost or latency is too high.
  [↗ Page](https://agentscamp.com/skills/performance/prompt-cache-optimizer) · `npx agentscamp add skills/prompt-cache-optimizer`

## Refactor

- **[Dead Code Finder](skills/dead-code-finder/SKILL.md)** — Find genuinely unused code — unreferenced exports, unreachable files, and unused dependencies — and remove it safely with build/test verification. Use when trimming a codebase or untangling years of accreted cruft.
  [↗ Page](https://agentscamp.com/skills/refactor/dead-code-finder) · `npx agentscamp add skills/dead-code-finder`

## Release

- **[Changelog From PRs](skills/changelog-from-prs/SKILL.md)** — Draft a release changelog by summarizing merged pull requests since the last tag. Use when preparing a release or writing release notes.
  [↗ Page](https://agentscamp.com/skills/release/changelog-from-prs) · `npx agentscamp add skills/changelog-from-prs`
