---
name: "accessibility-regression-auditor"
description: "Audit a UI change for accessibility regressions by combining automated checks with keyboard, focus, semantic, name-role-value, contrast, zoom, and screen-reader-oriented inspection. Use when reviewing a component or pull request, adding a dialog or form, changing navigation, or investigating an accessibility failure that a linter alone cannot explain."
allowed-tools: "Read, Grep, Glob, Bash"
version: 1.0.0
---

Review the changed user journey, not just the component markup or automated score.

## Workflow

1. **Define the affected journey.** Identify changed pages, components, states, breakpoints, input methods, and user actions. Include loading, empty, error, validation, success, and disabled states.
2. **Run project-native automation.** Use configured linters, component tests, browser tests, or accessibility scanners. Preserve tool versions, routes, rules, and raw violations. Treat automation as one evidence layer.
3. **Inspect semantics first.** Prefer native controls and landmarks. Verify heading order, labels, descriptions, table relationships, lists, link purpose, and name-role-value. Flag ARIA that replaces or contradicts native behavior.
4. **Trace keyboard operation.** Check reachability, visible focus, logical order, activation, escape behavior, focus trapping, roving tabindex where appropriate, and return of focus after dialogs or transient UI closes.
5. **Check dynamic communication.** Verify validation errors, async completion, toasts, expanded state, live regions, and route changes are announced without stealing focus or repeating excessively.
6. **Review visual access.** Check text and non-text contrast, focus indicators, 200% zoom, narrow reflow, text spacing, target size, motion preferences, and information conveyed only by color, position, hover, or animation.
7. **Exercise a representative assistive path.** When browser or platform tools are available, inspect the accessibility tree and test the critical flow with a screen-reader-oriented sequence. Do not claim device coverage that was not performed.
8. **Prioritize and regress.** Rank findings by blocked task and affected population. For deterministic defects, recommend the smallest automated regression check; retain manual steps for behavior automation cannot prove.

> [!WARNING]
> A zero-violation automated scan is not a pass. A perfectly valid button named “button” can still make a workflow unusable.

## Output

Provide the audited scope, environments and tools, findings with element or file evidence, affected interaction, severity, recommended remediation, and exact verification step. Separate automated, manual, and untested coverage.
