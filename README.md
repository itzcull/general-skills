# General Agent Skills

General-purpose [Agent Skills](https://agentskills.io/) that do not belong to a narrower domain repository.

Each installable skill is a direct child of `skills/`. A skill contains `SKILL.md` and only the support files its instructions use.

## Local installation

### Pi

Add `~/skills/general/skills` to the `skills` array in `~/.pi/agent/settings.json`.

### Codex

```bash
mkdir -p ~/.agents/skills
for skill in ~/skills/general/skills/*; do
  [ -f "$skill/SKILL.md" ] && ln -s "$skill" ~/.agents/skills/"${skill##*/}"
done
```

## Available skills

| Skill | Purpose |
| --- | --- |
| [writing-for-agents](skills/writing-for-agents/) | Create and evaluate reliable machine-consumed instructions. |
| [writing-for-humans](skills/writing-for-humans/) | Create informational writing readers can find, understand, and use. |
| [write-like-will](skills/write-like-will/) | Draft messages that Will sends under his own name, in his voice. |
| [knowledge-engineering](skills/knowledge-engineering/) | Structure documentation and context files around a single source of truth. |
| [humanizer](skills/humanizer/) | Remove AI writing patterns from prose. A verbatim copy of [blader/humanizer](https://github.com/blader/humanizer) (MIT). |

## License

[MIT](LICENSE)
