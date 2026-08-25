---
name: "cache-policy-designer"
description: "Design a cache policy from data ownership, freshness, privacy, invalidation, and failure requirements across browser, CDN, reverse-proxy, application, and data caches. Use when adding caching, debugging stale responses, reviewing Cache-Control behavior, reducing origin load, or deciding whether a value can be cached safely at all."
allowed-tools: "Read, Grep, Glob, Bash"
version: 1.0.0
---

Design caching as a correctness contract with a performance benefit.

## Workflow

1. **Inventory the cacheable object.** Name the response or value, authoritative source, readers, writers, sensitivity, size, cost to recompute, and consequence of serving it stale.
2. **Map every cache layer.** Trace browser, service worker, CDN, gateway, reverse proxy, framework, application, ORM, and database caches. Record which layer currently owns freshness and invalidation.
3. **Define identity and variation.** Specify the complete cache key: resource, tenant, user or authorization class, locale, encoding, version, query shape, and any header that changes representation. Remove unnecessary variants but never collapse security boundaries.
4. **Choose freshness semantics.** Set max age from the business freshness bound, not a convenient round number. Decide whether revalidation, `stale-while-revalidate`, or `stale-if-error` preserves acceptable behavior.
5. **Design invalidation.** Identify every write or event that changes the object. Choose purge, versioned keys, tag invalidation, write-through, or bounded expiration, and state how missed events heal.
6. **Control concurrency.** Prevent cold-key stampedes with request coalescing, locks with bounded leases, probabilistic early refresh, or jitter. Define behavior when the origin is slow or unavailable.
7. **Specify privacy and failure rules.** Mark values that must never enter a shared cache. Define fail-open versus fail-closed, negative caching, error caching, and the maximum stale age during outages.
8. **Verify and observe.** Test hit, miss, revalidation, invalidation, authorization variation, purge failure, origin failure, and concurrent expiry. Measure hit ratio by status, age, evictions, origin savings, stale serves, and key cardinality.

> [!WARNING]
> Do not add `public` caching or omit authorization from a key merely to improve hit rate. Cross-user cache leakage is a security failure, not a tuning tradeoff.

## Output

Return a layer-by-layer policy with key dimensions, freshness directives, invalidation events, stampede controls, outage behavior, privacy exclusions, implementation locations, verification cases, and metrics. Call out unknown writers or variation inputs that block safe caching.
