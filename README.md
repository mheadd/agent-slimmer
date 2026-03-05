# Agent Slimmer

An AI coding agent skill for optimizing `AGENTS.md` files (and similar repository-level context files like `CLAUDE.md`, `COPILOT.md`, etc.).

## Why

Research shows that repository-level context files measurably change AI coding agent behavior — but more content isn't better. Overly comprehensive files increase inference cost and can *reduce* task success rates. The most effective context files are short, specific, and contain only instructions that change agent behavior in ways the project actually requires.

Agent Slimmer encapsulates findings from two peer-reviewed studies into a reusable skill that evaluates and rewrites context files to their minimum effective form.

### Research basis

- **Lulla et al. (2026)** — *On the Impact of AGENTS.md Files on the Efficiency of AI Coding Agents* ([arXiv](https://arxiv.org/pdf/2601.20404)): Focused context files reduced agent completion time by ~28% and output tokens by ~17%.
- **Gloaguen et al. (2026)** — *Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents?* ([arXiv](https://arxiv.org/pdf/2602.11988)): LLM-generated context files reduced task success by 3% and increased cost by 20%+. Unnecessary instructions measurably degrade performance.

## Usage

Point your AI coding agent at the skill file and provide an `AGENTS.md` (or equivalent) to optimize:

```
Use the skill in agent-slimmer/slim-agents.md to optimize my AGENTS.md file.
```

The skill will evaluate the file against research-backed criteria, flag content that should be removed or revised, and produce an optimized version.

## What the skill does

1. **Identifies and removes** codebase descriptions the agent could discover on its own (directory trees, component summaries, architecture overviews)
2. **Identifies and removes** content that duplicates existing repository documentation (README, CONTRIBUTING, inline docs)
3. **Preserves and sharpens** behavioral instructions — specific tools, workflows, and constraints the agent wouldn't infer from the code
4. **Flags** vague or generic instructions that add cognitive load without directing behavior
5. **Produces** a slimmed-down file focused on minimum effective dose

## License

MIT
