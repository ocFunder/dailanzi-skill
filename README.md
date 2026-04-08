# 抽象带篮子 Skill

一个可直接安装的中文文案风格 Skill：把普通表达改写成“抽象、带梗、带节奏、可发布”的版本，并内置语料增强与风险分层。

## 功能亮点

- 多场景改写：评论区、短视频字幕、口播稿、通用文案。
- 默认输出：放飞版本（可按需指定稳妥/标准）。
- 证据驱动：内置 `references/research/` 语料与来源锚点。
- 风险可控：`v2 labeled` 语料含 `risk_score`，默认仅采样 `risk<=1`。

## 安装

### 1) 从 GitHub 安装（推荐）

```bash
npx skills add mri166/dailanzi-skill -y -g
```

### 2) 本地开发模式

将本仓库内容拷贝到：

```bash
~/.codex/skills/chouxiang-dailanzi-framework
```

## 触发词（示例）

- 抽象带篮子
- 带梗改写
- 评论区神回复
- 口播稿抽象化
- 整活文案 / 发癫文学

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
