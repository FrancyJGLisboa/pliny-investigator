# Pliny Investigator

An agent skill for evidence-grounded investigation. It reconstructs the real goal, challenges consequential assumptions, compares a simple alternative, and proposes the smallest reversible test (WHY → WHY NOT → TRY).

Modes: `--quick` (default), `--deep`, `--critic`, `--experiment`. See [`skills/pliny-investigator/SKILL.md`](skills/pliny-investigator/SKILL.md).

## Install

### GitHub Copilot CLI

```sh
# Personal (all projects): installs into ~/.copilot/skills/
gh skill install FrancyJGLisboa/pliny-investigator pliny-investigator --agent github-copilot --scope user

# Project only: run inside your repository
gh skill install FrancyJGLisboa/pliny-investigator pliny-investigator --agent github-copilot
```

Manual option: copy `skills/pliny-investigator/` to `~/.copilot/skills/pliny-investigator/` or to `.github/skills/pliny-investigator/` in a repository.

Restart Copilot CLI after the install. Then run `/skills list` to confirm that the skill loaded.

### Claude Code

```sh
gh skill install FrancyJGLisboa/pliny-investigator pliny-investigator --agent claude-code --scope user
```

Manual option: copy `skills/pliny-investigator/` to `~/.claude/skills/pliny-investigator/`.

### Codex CLI and other agents

```sh
gh skill install FrancyJGLisboa/pliny-investigator pliny-investigator --agent codex --scope user
```

For ChatGPT and fallbacks without skill support, see [`references/runtime-adapters.md`](skills/pliny-investigator/references/runtime-adapters.md).

## Usage

```text
Use pliny-investigator --quick: should we add a vector database to this prototype?
Use pliny-investigator --deep: investigate the assumptions behind this ETL architecture; do not modify files.
Use pliny-investigator --critic: independently challenge this design proposal.
Use pliny-investigator --experiment: design a falsifiable comparison of the current model vs a simpler baseline.
```

## Layout

```text
skills/pliny-investigator/
├── SKILL.md                      # the skill (name + description frontmatter)
├── references/
│   ├── findings-report.md        # output contract for DEEP/CRITIC/EXPERIMENT
│   └── runtime-adapters.md       # per-tool install notes
└── agents/openai.yaml            # ChatGPT display metadata
```
