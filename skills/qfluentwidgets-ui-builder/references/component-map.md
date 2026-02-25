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

## Mapping Rule

For every selected component, return:
1. Why chosen over alternatives
2. Official doc URL
3. Official example path
4. Local module placement suggestion
