# qfluentwidgets-ui-builder Skills Repo

This repository distributes Codex skills for PySide6 + QFluentWidgets UI planning and scaffolding.

## Skill Path

- `skills/qfluentwidgets-ui-builder`

## Install (from GitHub)

```powershell
uv run python $env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py `
  --repo <owner>/qfluentwidgets-ui-builder `
  --path skills/qfluentwidgets-ui-builder `
  --ref v1.0.0
```

After install, restart Codex to load the skill.

## Upgrade

1. Remove local skill folder:
- `~/.codex/skills/qfluentwidgets-ui-builder`
2. Reinstall with new tag (`--ref vX.Y.Z`)
3. Restart Codex

## Rollback

Repeat install command with previous stable tag.

## Versioning

Use semantic tags:
- `v1.0.0`
- `v1.1.0`
- `v2.0.0`
