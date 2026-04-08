# 抽象带篮子 Skill

一个可直接安装的“带篮子人格对话” Skill：默认直接和用户对话，按需切换成放飞文案，并内置语料增强与风险分层。

## 功能亮点

- 默认人格对话：先聊观点和态度，再按需改写文案。
- 默认风格：放飞版本（可按需指定稳妥/标准）。
- 证据驱动：内置 `references/research/` 语料与来源锚点。
- 风险可控：`v2 labeled` 语料含 `risk_score`，默认仅采样 `risk<=1`。

## 安装

### 1) 从 GitHub 安装（推荐）

```bash
npx skills add ocFunder/dailanzi-skill -y -g
```

### 2) 本地开发模式

将本仓库内容拷贝到：

```bash
~/.codex/skills/chouxiang-dailanzi-framework
```

## 对话方式（示例）

- 直接问它：这事你怎么看？
- 让它回你：给我一句能怼回去的。
- 需要时再补充：帮我改成评论区神回复 / 口播稿。

## 目录结构

```text
dailanzi-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── style-playbook.md
│   ├── platform-contexts.md
│   ├── mental-models-heuristics.md
│   ├── safety-boundaries.md
│   └── research/
│       ├── 00-method-and-scope.md
│       ├── 01-quotes-evidence.md
│       ├── 02-scene-index.md
│       ├── 03-style-signals.md
│       ├── 04-risk-boundaries.md
│       ├── 05-corpus-v1.md
│       ├── 06-corpus-v1-curated.md
│       ├── 07-corpus-v2-labeled.md
│       ├── raw-corpus.jsonl
│       ├── raw-corpus-curated.jsonl
│       └── raw-corpus-v2-labeled.jsonl
├── README.md
├── README_EN.md
└── LICENSE
```

## 版本说明

- `v1`：规则驱动 + 基础语料。
- `v1 curated`：高精度过滤，降低噪声。
- `v2 labeled`：逐条标签 + 风险分，可直接做采样策略。

## 合规与边界

- 本项目用于风格研究与文案改写，不用于人身攻击、歧视、网暴。
- 语料中“社区传播句”不等同“逐字首发原话”。
- 如用于品牌/商务场景，建议固定使用 `risk<=1`。

## 致谢

- 灵感与方法参考：[nuwa-skill](https://github.com/alchaincyf/nuwa-skill)

## License

MIT
