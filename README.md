# subscription-splitter 🧭 订阅系统拆分与边界设计器

> A **Codex skill** for correct module-boundary and split decisions in subscription/billing
> systems — classify every concept by **when it lives** (immutable fact, derived state,
> liability, future trigger) before deciding how to build or split it. Docs are in Chinese.

<p align="center">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-blue.svg"></a>
  <img alt="Version" src="https://img.shields.io/badge/version-v0.1.0-informational">
</p>

核心立场：**先问"它活在哪个时间"，再谈怎么建、怎么拆。**
订单/支付是写进历史的 ink（不可变事实），会员/权益是从 ink 投影出的影子（派生状态，可重建），
订阅是定期往纸上滴 ink 的机器（策略），积分是单独一本债簿（追加式账本）。

## 快速开始

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/Henri-lab/subscription-splitter.git ~/.codex/skills/subscription-splitter
```

之后在任意 Codex 会话中按 skill 名（`subscription-splitter`）触发即可。

## 目录

```text
SKILL.md                     主入口：时间模型 → 访谈 → 档位 D0~D3 → 拆分判据
agents/openai.yaml           agent 元数据
assets/                      边界决策报告模板
references/
├── time-model.md            六个概念的时间属性（事实/派生/负债/触发器）
├── boundary-rules.md        拆分四问 + 三个灵魂拷问 + 正反例
├── solution-tiers.md        访谈与档位矩阵 D0~D3
├── lessons-log.md           经验账本（L-001 起）
└── maintenance.md           技能持续进化纪律
```

## 三个不寻常之处

1. **时间是第一维度**：先分类（事实/派生/负债/触发器），再建模；
2. **拆分是举证责任**：默认不拆，三个灵魂拷问任一答错不得拆；
3. **订阅不是服务**：它是订单管道的"自动水龙头"——同一套管道喂人手点与机器点。

## 起源与署名

2026-10-16 整理为公开仓库，是 [membership-system-builder](https://github.com/Henri-lab/membership-system-builder)
的边界决策层。作者清单见 [AUTHORS.md](AUTHORS.md)；二次分发须保留 [LICENSE](LICENSE) 版权声明。

```text
subscription-splitter（v0.1.0）
作者：henrifox
仓库：https://github.com/Henri-lab/subscription-splitter
首发：2026-10-16｜许可：MIT（保留署名）
```

## License

[MIT](LICENSE) © 2026 henrifox
