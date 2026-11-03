# Runtime adapters

## ChatGPT
Install the ZIP as a skill where custom skills are supported or use the contents of SKILL.md as Project instructions. Invoke: `Use pliny-investigator --deep to challenge this proposal: ...` Availability of direct skill upload depends on the product surface/account. Do not imply the archive is already installed.

## Claude Code
For environments supporting Claude Code skills, place the skill folder in an appropriate skill location (commonly `.claude/skills/pliny-investigator/` for a project or `~/.claude/skills/pliny-investigator/` for personal use). Keep `SKILL.md` in place. If skill discovery differs in the installed version, inspect its documentation. For persistent lightweight guidance instead, add this to `CLAUDE.md`:

> For ambiguous research and architecture decisions, reconstruct the real goal, challenge consequential assumptions with evidence, compare a simple alternative, and propose the smallest reversible test. Use pliny-investigator on explicit request; do not run it on routine edits.

## Codex CLI
In Codex installations supporting custom skills, use the appropriate skill discovery location (commonly `.agents/skills/pliny-investigator/` for project or `$HOME/.agents/skills/pliny-investigator/` for user). Verify with the actual Codex version. Otherwise keep a compact version in `AGENTS.md`:

> For ambiguous research and architecture decisions, reconstruct the real goal, challenge consequential assumptions with evidence, compare a simple alternative, and propose the smallest reversible test. Use pliny-investigator on explicit request; do not run it on routine edits.

## GitHub Copilot CLI
Copilot CLI discovers skills in these locations:
- Project: `.github/skills/pliny-investigator/`, `.claude/skills/pliny-investigator/`, or `.agents/skills/pliny-investigator/`.
- Personal: `~/.copilot/skills/pliny-investigator/` or `~/.agents/skills/pliny-investigator/`.

Install with GitHub CLI: `gh skill install FrancyJGLisboa/pliny-investigator pliny-investigator --agent github-copilot`. Copilot selects the skill from its description. To force it, name the skill in the prompt. Without skill support, put the compact instruction below in `.github/copilot-instructions.md` or `AGENTS.md`:

> For ambiguous research and architecture decisions, reconstruct the real goal, challenge consequential assumptions with evidence, compare a simple alternative, and propose the smallest reversible test. Use pliny-investigator on explicit request; do not run it on routine edits.

## Usage examples
- `Use pliny-investigator --quick: should we add a vector database to this prototype?`
- `Use pliny-investigator --deep: investigate the assumptions behind this geospatial ETL architecture; do not modify files.`
- `Use pliny-investigator --critic: independently challenge this design proposal, focusing on leakage and decision validity.`
- `Use pliny-investigator --experiment: design a falsifiable comparison of current model vs simpler baseline; propose only.`
