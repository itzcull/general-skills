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

## License

[MIT](LICENSE)
