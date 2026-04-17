# Review Checklist

Run this checklist before final output.

## Evidence

1. Every major component includes official doc URL.
2. Every major component includes official example path when available.
3. Source priority follows `source-index.md`.

## Design quality

1. Route keys are explicit and unique.
2. File and module boundaries are explicit.
3. In scope and out of scope are explicit.
4. Risks and mitigations are explicit.

## Visual consistency

1. Theme initialization strategy is explicit.
2. Surface or background strategy is explicit for pages, cards, and scroll containers.
3. No native `QLabel` is left as a planned final visible label without justification.
4. Plain `QWidget` is not assigned a visible surface role by accident.
5. Long-path layout risk is handled when file or directory inputs exist.

## Implementation quality

1. Includes minimal runnable skeleton requirement.
2. Includes acceptance criteria.
3. Includes smoke test and behavior test scenarios.
4. Includes assumptions and defaults.
5. Includes visible label strategy.
6. Includes worker lifecycle and button state transitions when async tasks exist.

## Interaction quality

1. Run actions recover to a usable state after both success and failure.
2. Progress indicator visibility matches worker lifecycle.
3. Success and failure feedback are visible and non-blocking where appropriate.
4. Save or export actions have an explicit enablement rule when task results are required.

## Output quality

1. Uses the two-section output contract.
2. No unresolved high-impact decisions left to implementer.
