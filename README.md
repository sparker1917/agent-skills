# Agent Skills

Each reusable agent skill lives in its own folder under `skills/` and starts with a `SKILL.md` that tells the agent when and how to use it.

## Available skills

| Skill | Use it for |
| --- | --- |
| [WSWS Article Drafting](skills/wsws-article-drafting/SKILL.md) | Draft or revise World Socialist Web Site–style articles using sourced reporting, Marxist class analysis, and an internationalist perspective. |

## Use in Codex

From the root of this checkout, copy the skill into your Codex skills directory.

```sh
skills_dir="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skills_dir"
cp -R skills/wsws-article-drafting "$skills_dir/"
```

Invoke `$wsws-article-drafting` in Codex. If the skill does not appear, restart Codex. Include the article type, topic, and any source material you want the draft to use.

> Use $wsws-article-drafting to draft a news analysis from the attached strike notices and contract summary. Flag claims that still need a source.

## Add a skill

Create `skills/<skill-name>/SKILL.md` with YAML frontmatter containing a `name` that matches the folder and a `description` that explains when the skill applies. Keep the instructions in that file and link any supporting resources from it. Add the skill to the table above.
