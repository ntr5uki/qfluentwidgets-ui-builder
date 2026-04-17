# Component Map

## Navigation and Window

1. Multi-page shell with side navigation
- Component: `MSFluentWindow`
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/latest/autoapi/qfluentwidgets/window/fluent_window/index.html
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/window/ms_fluent_window
- Adaptation: register pages via `addSubInterface`, set default item by route or objectName

2. Tree or complex navigation
- Component: `FluentWindow` with navigation tree
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/latest/autoapi/qfluentwidgets/window/fluent_window/index.html
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/window/fluent_window
- Adaptation: use parent route relationships for nested pages

## Data Display

1. Data table viewer
- Component: `TableView`
- Doc: https://qfluentwidgets.com/zh/pages/components/tableview/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/view
- Adaptation: start with simple model, then pagination and filtering

2. List browsing
- Component: `ListView`
- Doc: https://qfluentwidgets.com/zh/pages/components/listview/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/view
- Adaptation: pair with search or filter bar

3. Tree data
- Component: `TreeView`
- Doc: https://qfluentwidgets.com/zh/pages/components/treeview/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/view
- Adaptation: use only when hierarchy is real

## Forms and Settings

1. Settings hub
- Component: `SettingCard` family
- Doc: https://qfluentwidgets.com/zh/pages/components/settingcard/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/window/settings
- Adaptation: separate UI model and persistence model

2. Text input
- Component: `LineEdit`
- Doc: https://qfluentwidgets.com/zh/pages/components/lineedit/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/text
- Adaptation: centralize validation rules

3. Option input
- Component: `ComboBox`, `SwitchButton`, `SpinBox`
- Doc: https://qfluentwidgets.com/zh/pages/components/combobox/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/basic_input
- Adaptation: preserve defaults and reset strategy

4. Visible form labels
- Component: `CaptionLabel`, `BodyLabel`, `StrongBodyLabel`
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/stable/autoapi/qfluentwidgets/components/widgets/label/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/text
- Adaptation: create labels explicitly in forms; do not depend on `QFormLayout.addRow(str, widget)` for final visible text

5. Long-path fields
- Component: `LineEdit` plus elide and tooltip strategy
- Doc: https://qfluentwidgets.com/zh/pages/components/lineedit/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/text
- Adaptation: preserve full path in state, show shortened text when width is constrained, and set tooltip to the full value

## Theme and Surface Consistency

1. Theme initialization
- Component: `setTheme`, `Theme`
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/latest/theme.html
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples
- Adaptation: define theme mode at app startup and avoid leaving light/dark behavior implicit

2. Page and group surfaces
- Component: `CardWidget`, `SettingCard`
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/latest/autoapi/qfluentwidgets/components/widgets/card_widget/index.html
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/window/settings
- Adaptation: treat cards as content surfaces, not as guaranteed opaque background replacement; define what sits behind them

3. Scrollable page containers
- Component: `SmoothScrollArea`
- Doc: https://pyqt-fluent-widgets.readthedocs.io/zh-cn/stable/autoapi/qfluentwidgets/components/widgets/scroll_area/index.html
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/scroll
- Adaptation: when a scroll viewport is visible, make its background policy explicit and prefer transparent handling over default Qt white surfaces

## Feedback and Status

1. Non-blocking notification
- Component: `InfoBar`
- Doc: https://qfluentwidgets.com/zh/pages/components/infobar/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/status_info
- Adaptation: map severity to operation result codes

2. Progress feedback
- Component: `ProgressBar`, `ProgressRing`
- Doc: https://qfluentwidgets.com/zh/pages/components/progressbar/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/status_info
- Adaptation: connect to long-running task state

3. Confirm dialogs
- Component: `MessageBox`
- Doc: https://qfluentwidgets.com/zh/pages/components/messagebox/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/dialog_flyout
- Adaptation: reserve for destructive actions

4. Task-state feedback
- Component: `ProgressRing` plus `InfoBar`
- Doc: https://qfluentwidgets.com/zh/pages/components/progressbar/
- Example: https://github.com/zhiyiYo/PyQt-Fluent-Widgets/tree/PySide6/examples/status_info
- Adaptation: map worker states to button enablement, progress visibility, success message, failure message, and rerun readiness

## Pitfalls and Adaptation Notes

1. `CardWidget` can be semi-transparent in dark themes; do not assume it hides an unfitted base background.
2. `QScrollArea` and its `viewport()` can leak native Qt background unless surface handling is explicit.
3. `QFormLayout.addRow(str, widget)` creates a native `QLabel`; use Fluent labels for final visible text hierarchy.
4. Plain `QWidget` is fine for structure, but should usually stay transparent if it is not the intended visual surface.
5. Long file and directory paths need elide, tooltip, and width constraints before layout freeze.

## Mapping Rule

For every selected component, return:
1. Why chosen over alternatives
2. Official doc URL
3. Official example path
4. Local module placement suggestion
5. Theme or surface implications when the component is user-visible
