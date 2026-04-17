---
name: qfluentwidgets-ui-builder
description: Plan and scaffold PySide6/QFluentWidgets desktop interfaces with official doc mappings and reusable patterns. Use when users ask to start, redesign, or extend QFluentWidgets screens, navigation, settings, data viewers, or project skeletons.
---

# QFluentWidgets UI Builder

## Overview

Use this skill to design and scaffold PySide6 plus QFluentWidgets interfaces quickly and consistently.
Deliver implementation-ready outputs instead of generic advice.

## Workflow

1. Normalize requirement inputs:
- Read `references/requirement-template.md`
- Capture required fields before architecture decisions

2. Select a layout pattern:
- Read `references/layout-patterns.md`
- Choose one base window and navigation pattern
- Lock route keys and page responsibilities

3. Map requirements to components:
- Read `references/component-map.md`
- For each interaction, provide:
  - official doc URL
  - official example path
  - local adaptation notes

4. Audit theme and visible surfaces:
- Define theme initialization strategy with `setTheme(...)` when theme requirements exist
- Decide page background, scroll viewport, and card/container surface behavior
- Check that user-visible labels stay in the Fluent label family
- Check long-path, narrow-sidebar, and stacked-card layout risks
- If async work exists, define worker lifecycle and button/status state transitions

5. Ground references:
- Read `references/source-index.md`
- Always prioritize sources in defined order
- Avoid unsupported or unverified API suggestions

6. Produce standard output:
- Read `references/output-contract.md`
- Return two sections by default:
  - Design Plan
  - Code Plan
- Keep output decision-complete for implementation

7. Run quality self-check:
- Read `references/review-checklist.md`
- Ensure all required evidence and acceptance items are present

## Output Rules

1. Always include explicit file and module boundaries.
2. Always include acceptance criteria and test scenarios.
3. Default to a minimal runnable skeleton first, then incremental feature extension.
4. If requirements are ambiguous, ask minimal high-impact clarifying questions.
5. Include theme/surface strategy and visible label strategy when UI surfaces are user-facing.
6. Include worker state transitions and recovery rules when background tasks exist.

## Guardrails

1. Do not mix Qt-binding variants of Fluent packages in one environment.
2. Do not treat upstream examples as direct dependencies.
3. Prefer stable package install path (`PySide6` plus `PySide6-Fluent-Widgets`).
4. Qt layouts may be mixed freely, but user-visible controls should default to QFluentWidgets components.
5. Plain `QWidget` may be used as structure or transparent container, but should not provide the final visible surface by accident.
6. Prefer `CaptionLabel`, `BodyLabel`, or `StrongBodyLabel` for visible form labels; do not rely on `QFormLayout.addRow(str, widget)` auto-generated labels.
7. When scroll containers are visible, prefer `SmoothScrollArea` or explicitly define viewport background handling.
8. When background tasks exist, define `idle -> running -> success/failure -> ready-to-rerun` transitions before implementation.
9. For file or directory paths, define elide, tooltip, and width constraints before choosing the final field layout.
10. Keep the first implementation simple and extensible.

## References

- Source index: `references/source-index.md`
- Requirement template: `references/requirement-template.md`
- Component mapping: `references/component-map.md`
- Layout patterns: `references/layout-patterns.md`
- Output contract: `references/output-contract.md`
- Review checklist: `references/review-checklist.md`
- End-to-end cases: `references/cases.md`
