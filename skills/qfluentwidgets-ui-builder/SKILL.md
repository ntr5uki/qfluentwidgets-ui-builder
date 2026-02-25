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
- Goal and target users
- Screens and pages
- Core interactions
- Data volume and constraints
- In scope and out of scope

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

4. Ground references:
- Read `references/source-index.md`
- Always prioritize sources in defined order
- Avoid unsupported or unverified API suggestions

5. Produce standard output:
- Read `references/output-contract.md`
- Return two sections by default:
  - Design Plan
  - Code Plan
- Keep output decision-complete for implementation

## Output Rules

1. Always include explicit file and module boundaries.
2. Always include acceptance criteria and test scenarios.
3. Default to a minimal runnable skeleton first, then incremental feature extension.
4. If requirements are ambiguous, ask minimal high-impact clarifying questions.

## Guardrails

1. Do not mix Qt-binding variants of Fluent packages in one environment.
2. Do not treat upstream examples as direct dependencies.
3. Prefer stable package install path (`PySide6` plus `PySide6-Fluent-Widgets`).
4. Keep the first implementation simple and extensible.

## References

- Source index: `references/source-index.md`
- Component mapping: `references/component-map.md`
- Layout patterns: `references/layout-patterns.md`
- Output contract: `references/output-contract.md`
