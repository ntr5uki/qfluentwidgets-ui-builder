# Changelog

## v1.1.0

### Added
- Added `references/requirement-template.md` for structured input collection.
- Added `references/review-checklist.md` for pre-output quality checks.
- Added `references/cases.md` with three end-to-end prompt examples.
- Added `assets/icon-small.svg` and `assets/icon-large.svg`.
- Added `policy.allow_implicit_invocation` and UI metadata fields in `agents/openai.yaml`.
- Added theme and surface consistency guidance across `SKILL.md` and references.
- Added parameter-heavy desktop tuning tool case to `references/cases.md`.

### Changed
- Updated `SKILL.md` workflow to include requirement template and review checklist steps.
- Replaced ambiguous `same window API page` with explicit URL in `component-map.md`.
- Updated `layout-patterns.md` placeholder from `<app>` to `<package_name>` and added real path example.
- Updated `output-contract.md` with minimal runnable code block requirements.
- Expanded `component-map.md` with Fluent label guidance, surface handling, task-state mapping, and long-path field strategy.
- Expanded `output-contract.md` and `review-checklist.md` with theme, surface, label, and worker state expectations.

### Fixed
- Reduced ambiguity in component reference wording and adaptation notes.

### Breaking
- Default policy now sets `allow_implicit_invocation: false`; explicit invocation is expected.

## v1.0.0

### Added
- Initialized `qfluentwidgets-ui-builder` skill.
- Added base references:
  - source-index
  - component-map
  - layout-patterns
  - output-contract
- Added installation guide for GitHub distribution.
