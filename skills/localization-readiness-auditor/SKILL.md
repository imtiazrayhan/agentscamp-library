---
name: "localization-readiness-auditor"
description: "Audit an application or feature for localization readiness across extracted messages, interpolation, pluralization, date and number formatting, layout expansion, right-to-left behavior, sorting, search, assets, metadata, and test coverage. Use before adding a locale, reviewing hard-coded UI text, or investigating a feature that breaks outside English."
allowed-tools: "Read, Grep, Glob, Bash"
version: 1.0.0
---

Find assumptions that make a feature work only for one language or region.

## Workflow

1. **Define target surfaces.** Identify platforms, routes, components, notifications, documents, emails, metadata, accessibility labels, server messages, and locales or writing systems in scope.
2. **Inventory user-facing text.** Find hard-coded strings, concatenation, duplicated messages, image text, backend-provided prose, placeholders, and strings assembled from fragments. Preserve translator context and stable identifiers.
3. **Check message grammar.** Verify interpolation, plural and select rules, gender or grammatical variants where required, markup handling, escaping, and full-sentence translation. Avoid English word-order assumptions.
4. **Inspect locale-aware data.** Review date, time, timezone, calendar, number, currency, percentage, address, name, phone, unit, collation, and case conversion behavior. Keep storage formats separate from presentation.
5. **Test input and text processing.** Exercise Unicode, composed and decomposed characters, non-Latin scripts, emoji, long names, input methods, normalization, validation, truncation, search, slugs, exports, and round trips.
6. **Stress layout.** Use a lengthened pseudolocale and narrow viewport to find fixed widths, clipping, overlapping controls, unsafe truncation, and text embedded in graphics. Verify zoom and dynamic type where supported.
7. **Inspect bidirectional behavior.** Test RTL direction, mirroring, mixed-direction text, icons with directional meaning, number and code isolation, focus order, gestures, and charts. Do not mirror brand marks or inherently fixed symbols.
8. **Review loading and fallback.** Check locale detection, explicit user choice, routing, bundle loading, fallback chains, missing-key telemetry, cached variation, server-client consistency, and SEO metadata.
9. **Define regression coverage.** Add or recommend pseudolocale builds, missing-key checks, representative locale tests, screenshots for critical layouts, and format assertions that avoid machine-specific locale defaults.

> [!WARNING]
> Translating visible strings does not make a feature localized if dates, plural rules, layout, search, validation, or screen-reader labels still assume English.

## Output

Report the audited surfaces and locales, blockers by user journey, hard-coded and structurally unsafe messages, formatting and Unicode defects, layout and RTL findings, fallback gaps, test recommendations, and evidence locations. Separate product copy questions from technical defects.
