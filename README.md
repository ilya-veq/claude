# claude

Personal Claude Code configuration.

## Skills

Installed under `.claude/skills/`, available to any Claude Code session started in this repo.

| Source | Skills | Pinned at |
| --- | --- | --- |
| [emilkowalski/skills](https://github.com/emilkowalski/skills) | `animate`, `animation-vocabulary`, `apple-design`, `ask-sonner`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `pick-ui-library`, `prototype`, `review-animations` | `78761e1` |
| [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | `impeccable` (23 sub-commands) + 4 `impeccable-*` agents in `.claude/agents/` | `251135e` (v4.0.4) |

Impeccable's optional design-detector hooks (`PostToolUse` on Edit/Write, `Stop`) are **not** installed. To add them, copy `.claude/settings.json` from the upstream repo. They require Node 22+.

### Updating

Re-run the upstream installers from this repo root, or re-copy by hand:

```bash
npx skills@latest add emilkowalski/skills
npx impeccable update
```
