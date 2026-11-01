# Upstream

`SKILL.md` is a verbatim copy of https://github.com/blader/humanizer (MIT, see LICENSE).

- Version: 2.11.2 (`metadata.version` in the frontmatter)
- Commit: e2e92e7b4b8229253ed5c8e81dc65463fdeddda5 (2026-08-19)
- Installed: 2026-09-02

Keep `SKILL.md` byte-identical to upstream so a refresh is a plain copy. Workspace-specific
rules (embedded mode always, ASCII-only overrides the writing-sample exception in section 14,
never add a fact) live in `CLAUDE.md` and the calling skills, not here.

Refresh:

    gh api repos/blader/humanizer/contents/SKILL.md --jq .content | base64 -d \
      > skills/humanizer/SKILL.md
    gh api repos/blader/humanizer/commits/main --jq '.sha, .commit.committer.date'

Then update the version, commit and date above.

This skill is client-agnostic. It is installed here as a real directory until it lands in
vectorise-core; once promoted and merged, `promote-to-core --finalize` swaps it for the
core symlink.
