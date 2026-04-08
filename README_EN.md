# Chouxiang Dailanzi Skill

A ready-to-install persona skill that talks like “Dailanzi” by default, and rewrites text only when needed, with evidence-backed corpus enhancement and risk controls.

## Highlights

- Persona-first conversation by default; rewriting on demand.
- Default style: Wild version (Safe/Standard only when requested).
- Evidence-backed references in `references/research/`.
- Risk-aware sampling with `risk_score` (default: use `risk<=1`).

## Installation

### 1) Install from GitHub

```bash
npx skills add ocFunder/dailanzi-skill -y -g
```

### 2) Local development

Copy this repo into:

```bash
~/.codex/skills/chouxiang-dailanzi-framework
```

## Trigger Examples

- 抽象带篮子
- meme rewrite
- comment reply rewrite
- short-video subtitle polish

## Structure

```text
SKILL.md
agents/openai.yaml
references/
references/research/
README.md
README_EN.md
LICENSE
```

## Compliance Notes

- For style research and copywriting assistance only.
- No harassment, hate, or targeted abuse.
- Community-spread phrases are not equal to first-source verbatim quotes.

## Credits

- Inspired by [nuwa-skill](https://github.com/alchaincyf/nuwa-skill)

## License

MIT
