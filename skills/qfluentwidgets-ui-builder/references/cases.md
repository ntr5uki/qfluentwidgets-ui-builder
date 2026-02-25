# End-to-End Cases

## Case 1: Minimal data viewer app

Prompt:
- Build a PySide6 QFluentWidgets desktop app with Home, Viewer, Config pages.
- First version should focus on skeleton only.

Expected output skeleton:
1. Design Plan with Pattern A.
2. Code Plan with `main.py`, `app.py`, `main_window.py`, and page modules.
3. Component mapping includes `MSFluentWindow`, `TableView`, `SettingCard`.

## Case 2: Task-oriented data tool

Prompt:
- Build an app for batch data processing with Dashboard, Tasks, Viewer, Logs, Settings.
- Need progress feedback and non-blocking notifications.

Expected output skeleton:
1. Design Plan with Pattern B.
2. Code Plan includes worker model and status mapping.
3. Component mapping includes `ProgressBar` or `ProgressRing`, `InfoBar`, `MessageBox`.

## Case 3: Settings-heavy desktop utility

Prompt:
- Build a desktop utility with strong settings management and import or export config.
- Keep first iteration minimal and testable.

Expected output skeleton:
1. Design Plan with Pattern C.
2. Code Plan includes settings schema and persistence boundary.
3. Component mapping includes `SettingCard` family and input controls.
