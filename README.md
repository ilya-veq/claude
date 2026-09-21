# claude

Personal Claude Code configuration.

## Skills

Installed under `.claude/skills/`, available to any Claude Code session started in this repo.

| Source | Skills | Pinned at |
| --- | --- | --- |
| [emilkowalski/skills](https://github.com/emilkowalski/skills) | `animate`, `animation-vocabulary`, `apple-design`, `ask-sonner`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `pick-ui-library`, `prototype`, `review-animations` | `78761e1` |
| [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | `impeccable` (23 sub-commands) + 4 `impeccable-*` agents in `.claude/agents/` | `251135e` (v4.0.4) |
| [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) | `design-taste-frontend` (the `taste-skill` folder, v2) | `5217fb4` |

The taste-skill repo bundles 13 skills; only `design-taste-frontend` is installed. The rest (`taste-skill-v1`, the GPT/Codex-targeted `gpt-taste` and `image-to-code`, the `imagegen-*` image-generation skills, and the other aesthetic presets) can be added with `--skill "<install name>"`.

`skills-lock.json` is written by the `npx skills` CLI and records only what that CLI installed.

Impeccable's optional design-detector hooks (`PostToolUse` on Edit/Write, `Stop`) are **not** installed. To add them, copy `.claude/settings.json` from the upstream repo. They require Node 22+.

### Updating

Re-run the upstream installers from this repo root, or re-copy by hand:

```bash
npx skills@latest add emilkowalski/skills
npx skills@latest add https://github.com/Leonxlnx/taste-skill --skill "design-taste-frontend" --agent claude-code --copy
npx impeccable update
```
