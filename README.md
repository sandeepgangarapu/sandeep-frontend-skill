# Sandeep Frontend Skill

Sandeep's personal front-end design skill for AI coding agents. It guides agents toward light-first, polished, subject-specific interfaces with compact hierarchy, useful pills, careful typography, strong copy, and non-generic design judgment.

The skill declares its inspirations once: Anthropic's frontend-design skill for its subject-grounded process, and Every.to for light editorial/product taste. The working guidance is Sandeep's own front-end language.

## What's Inside

```text
skills/sandeep-frontend/                 # Portable Agent Skill
plugins/sandeep-frontend/                # Plugin wrapper for marketplaces
.claude-plugin/marketplace.json          # Claude Code marketplace entry
.agents/plugins/marketplace.json         # Codex marketplace-style entry
SKILL.md                                 # Root copy for direct local use
references/design-language.md            # Detailed design language
agents/openai.yaml                       # Codex UI metadata
```

The skill is offline by default. It has no scripts, no API keys, no remote assets, and no network calls.

## Install in Claude Code

Claude Code supports Agent Skills as folders containing `SKILL.md`, and also supports adding a GitHub repo as a plugin marketplace.

Marketplace install:

```text
/plugin marketplace add sandeepgangarapu/sandeep-frontend-skill
/plugin install sandeep-frontend@sandeep-frontend-skill
```

After installing as a plugin, invoke it from Claude Code with:

```text
/sandeep-frontend:sandeep-frontend
```

Or ask naturally for Sandeep's front-end style.

Manual skill install:

```bash
git clone https://github.com/sandeepgangarapu/sandeep-frontend-skill.git
mkdir -p ~/.claude/skills
cp -R sandeep-frontend-skill/skills/sandeep-frontend ~/.claude/skills/
```

Then restart Claude Code if needed and invoke:

```text
/sandeep-frontend
```

## Install in Codex

Recommended direct skill install:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo sandeepgangarapu/sandeep-frontend-skill \
  --path skills/sandeep-frontend
```

Then restart Codex and invoke:

```text
$sandeep-frontend
```

Codex plugin-style install is also supported from the `plugins/sandeep-frontend` folder for environments that use marketplace/plugin manifests.

## Generic Agent Skills Install

This repo follows the common Agent Skills shape: a skill is a folder with a `SKILL.md` file and optional supporting resources. For any compatible agent, copy:

```text
skills/sandeep-frontend/
```

into that agent's skills directory.

## Usage Example

```text
Use $sandeep-frontend to redesign this dashboard in a light, polished, subject-specific style.
```

```text
Use /sandeep-frontend to make this data analysis page feel editorial but not generic.
```

## Example Output

- [AI Adoption Divide](examples/ai-adoption-divide.html): a single-file HTML example showing the skill's light editorial analysis mode for a data-analysis topic.

## Development

Validate the skill:

```bash
python ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py skills/sandeep-frontend
```

Validate the Codex plugin wrapper:

```bash
python ~/.codex/skills/.system/plugin-creator/scripts/validate_plugin.py plugins/sandeep-frontend
```

## References

- [Claude Code skills documentation](https://code.claude.com/docs/en/skills)
- [Anthropic Agent Skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [Anthropic public skills repository](https://github.com/anthropics/skills)
