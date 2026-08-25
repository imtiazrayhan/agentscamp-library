---
name: "release-readiness-reviewer"
description: "Review whether a specific release is ready to ship by checking scope, tests, compatibility, migrations, configuration, observability, rollout, rollback, support, security, and ownership against explicit evidence. Use before a production deployment, major version, risky feature launch, migration, or go/no-go meeting."
allowed-tools: "Read, Grep, Glob, Bash"
version: 1.0.0
---

Judge one release from current evidence and name what remains unresolved.

## Workflow

1. **Establish release identity.** Record artifact or commit, environment, intended time, included changes, excluded work, owners, risk class, and user impact. Reject a moving or ambiguous scope.
2. **Review change evidence.** Inspect diffs, tests, dependency and configuration changes, generated artifacts, feature flags, operational tasks, and known issues. Link every readiness claim to a source.
3. **Check compatibility.** Verify API, schema, event, SDK, client, runtime, and infrastructure compatibility across mixed versions and deploy order. Identify mandatory coordination.
4. **Assess data and configuration.** Review migrations, backfills, secrets, environment variables, defaults, capacity, region differences, and one-way transformations. Confirm target values without exposing credentials.
5. **Evaluate verification.** Require relevant automated and manual results, unresolved failures, representative environments, performance or load evidence where risk warrants, and post-deploy smoke tests.
6. **Confirm observability and support.** Name dashboards, alerts, logs, traces, business signals, on-call owner, escalation, status communication, customer support notes, and known symptom recognition.
7. **Review rollout and recovery.** Check stages, cohorts, bake times, promotion gates, abort thresholds, rollback mechanism, data compatibility, recovery time, and fallback when rollback is impossible.
8. **Issue the decision.** Choose go, conditional go, or no-go. List blockers separately from accepted risks, conditions, owners, deadlines, approval authority, and evidence that will close each item.

> [!WARNING]
> Do not turn unknowns into implicit acceptance. An unverified migration, missing owner, or untested rollback remains visible in the decision.

## Output

Return release identity, risk summary, evidence matrix, blockers, accepted risks, rollout and rollback readiness, observability and support readiness, decision, approvers, and time-bounded conditions. Include the exact post-deploy verification and abort signals.
