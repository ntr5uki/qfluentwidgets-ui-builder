# Output Contract

## Default Output Mode

Always provide two sections in this order:
1. Design Plan
2. Code Plan

## 1) Design Plan (required fields)

1. Goal and scope
2. Chosen layout pattern and why
3. Screen list and responsibilities
4. Component mapping table:
- requirement
- chosen component
- doc URL
- example path
- adaptation notes
5. Risks and mitigations
6. Acceptance criteria

## 2) Code Plan (required fields)

1. File tree
2. Public interfaces or classes or functions to add
3. Initialization and data flow sequence
4. Error handling strategy
5. Test scenarios (smoke plus behavior)
6. Rollout order
7. Minimal runnable code block requirement:
- include entry file
- include main window
- include at least one page module

## Quality Bar

1. Decision-complete: implementer should not make architecture decisions.
2. Traceable: every major component has official reference.
3. Minimal-first: runnable skeleton before advanced features.
4. Explicit assumptions: list defaults when user leaves gaps.
