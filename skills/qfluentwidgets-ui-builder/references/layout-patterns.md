# Layout Patterns

## Pattern A: Minimal 3-Page MSFluent Shell

Use when:
- Fast project bootstrap is required
- Requirements are still evolving

Default routes:
1. `home`
2. `viewer`
3. `config`

Suggested files:
1. `main.py`
2. `src/<app>/app.py`
3. `src/<app>/main_window.py`
4. `src/<app>/pages/base_page.py`
5. `src/<app>/pages/home_page.py`
6. `src/<app>/pages/viewer_page.py`
7. `src/<app>/pages/config_page.py`

## Pattern B: Data Tool with Task Workflow

Use when:
- Core value is data operations
- Needs task run status and logs

Default routes:
1. `dashboard`
2. `tasks`
3. `viewer`
4. `logs`
5. `settings`

Key additions:
- Background worker model
- Status page with progress and result summary

## Pattern C: Settings-Heavy Desktop App

Use when:
- Multiple configurable modules
- Need grouped setting cards and validation

Default routes:
1. `overview`
2. `modules`
3. `settings`
4. `about`

Key additions:
- Config schema and persistence adapter
- Import/export settings flow

## Selection Rule

1. Choose the simplest pattern that satisfies current scope.
2. Lock route keys early to reduce refactor cost.
3. Keep first iteration to skeleton + placeholders.
