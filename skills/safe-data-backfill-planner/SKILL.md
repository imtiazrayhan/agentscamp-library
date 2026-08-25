---
name: "safe-data-backfill-planner"
description: "Plan and implement a resumable production data backfill with bounded batches, checkpoints, rate limits, correctness verification, observability, and a pause or rollback path. Use when populating a new column, repairing historical rows, re-keying records, migrating derived data, or updating millions of records without overwhelming the database or replicas."
allowed-tools: "Read, Grep, Glob, Edit"
version: 1.0.0
---

Design the backfill as a controlled production workload. Keep schema changes, application compatibility, and the data job as separate deployable phases.

## Workflow

1. **Define source, target, and invariant.** State how the target value is derived, which rows qualify, how live writes behave during the job, and what must be true when complete.
2. **Establish rollout order.** Add the target shape first, deploy code that can read both shapes and writes the new shape, then backfill. Contract the old shape only after verification and an observation window.
3. **Choose a stable cursor.** Prefer an indexed immutable key such as primary key or creation ID. Use keyset pagination (`WHERE id > checkpoint ORDER BY id LIMIT n`), not offset pagination on a changing table.
4. **Make each batch bounded.** Limit rows, transaction time, lock wait, statement time, and concurrency. Commit after each batch. Add a small delay or adaptive rate control based on database load and replica lag.
5. **Make it resumable and idempotent.** Persist the high-water mark and counters. Reprocessing a batch must be safe. Update only eligible rows with a predicate such as `target IS NULL` or an expected version.
6. **Protect live writes.** Use compare-and-set conditions, version checks, or dual-write ordering so a batch computed from stale data cannot overwrite a newer application value.
7. **Instrument progress and impact.** Record scanned, updated, skipped, failed, retry, and remaining estimates; batch duration; lock waits; database CPU; WAL; replica lag; and affected application latency.
8. **Verify independently.** Compare eligible and completed counts, run invariant queries, sample records across the key range, and use checksums or aggregates when appropriate. Do not trust the job's own success counter alone.
9. **Define pause and recovery.** State thresholds that stop the job, how to resume from the checkpoint, how poison rows are quarantined, and whether correction means reverse transformation, restore, or forward repair.
10. **Clean up deliberately.** Remove dual-read or dual-write compatibility and old columns only after completion, verification, and a rollback-safe observation period.

> [!WARNING]
> Never use `OFFSET` as the progress cursor for a large changing dataset. Deletes, inserts, and updates can cause skipped or duplicated rows, and later pages become increasingly expensive.

## Output

Return:

- the expand/backfill/contract deployment sequence
- the job or migration code with stable cursor, batch transaction, checkpoint, and idempotent predicate
- batch size, concurrency, timeouts, and adaptive throttle rules
- metrics, dashboard queries, and automatic pause thresholds
- correctness queries and sampling plan
- crash recovery, poison-row handling, and rollback or forward-repair strategy
- completion and cleanup criteria
