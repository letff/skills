# Personal Codex Skills

个人维护的可复用 Codex 技能集合。每个技能是独立目录，包含必需的 `SKILL.md`，并可按需带有 `agents/`、`scripts/`、`references/` 或 `assets/`。

## 当前技能

| 技能 | 用途 |
| --- | --- |
| `workflow-selector` | 根据任务范围选择只读、快速、标准或复杂工作流，并按需加载辅助技能。 |
| `document-driven-development` | 按快速、标准或复杂档，以方案、进度、调整和成果文档驱动代码改动。 |
| `behavior-charter` | 提供停止条件、授权与验证闸门、来源标注和发送前检查。 |

## 目录结构

```text
.
├─ workflow-selector/
│  └─ SKILL.md
├─ behavior-charter/
│  └─ SKILL.md
├─ document-driven-development/
│  ├─ SKILL.md
│  └─ agents/
│     └─ openai.yaml
├─ README.md
└─ .gitignore
```

## 使用方式

将某个技能目录复制或链接到需要使用它的位置：

- 当前桌面环境的个人技能目录：`%USERPROFILE%\\.codex\\skills\\<技能名>`
- 项目专属技能目录：`<项目根目录>/.agents/skills/<技能名>`

例如，复制 `document-driven-development` 目录后，重新打开 Codex 或刷新技能列表即可使用。

推荐使用 `workflow-selector` 作为入口：只读任务直接处理；有实际修改时选择 DDD 快速、标准或复杂档。DDD 使用 `plan.md`、`progress.md`、`adjustments.md`、`continuation.md` 和 `outcome.md` 管理项目状态；通用 `handoff` 技能保持独立，项目级接续记录使用 `continuation.md`。

## 参考技能

`workflow-selector` 的工作流选择和职责划分参考了以下技能的公开定位与使用方式：

- `handoff`：会话级交接摘要；来自 [`mattpocock/skills`](https://github.com/mattpocock/skills/tree/main/skills/productivity/handoff) 的外部技能，保持独立，不随本仓库修改或发布。
- `document-driven-development`：项目级方案、进度、结果和跨会话接续记录；本仓库实际包含。
- `ponytail`：优先采用小而直接的改动，避免无必要的复杂化；外部 GitHub 技能，来源为 [`DietrichGebert/ponytail`](https://github.com/DietrichGebert/ponytail)。
- `behavior-charter`：授权边界、验证要求和事实与推断的区分；来源为 DSH `@ohtokaah-sys/dsh-charter@0.1.2`，当前未确认对应的公开 GitHub 地址。
- `i-have-adhd`：长任务的注意力和范围控制；来自 [`ayghri/i-have-adhd`](https://github.com/ayghri/i-have-adhd/tree/main/skills/i-have-adhd) 的外部技能。
- `karpathy-behavioral-guidelines`：假设、成功标准、最小修改和验证纪律；对应公开技能为 [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills) 中的 `karpathy-guidelines`，属于 Karpathy 风格指南的社区实现，并非 Andrej Karpathy 本人仓库。

目前能确认来源的其他人 GitHub 技能为 4 个：`handoff`、`ponytail`、`i-have-adhd` 和 `karpathy-guidelines`；`behavior-charter` 的来源仍未核实。参考不表示这些技能已被复制、安装或由本仓库维护。使用 `workflow-selector` 时，应先确认辅助技能在当前环境可发现；不可用时只采用相关的简短原则。

## 维护约定

- 每项技能保持独立目录和唯一的 `name`。
- 共享前删除令牌、内部地址、客户数据和个人绝对路径。
- 修改技能时更新对应的 `SKILL.md`；涉及桌面界面元数据时同步更新 `agents/openai.yaml`。
- 提交信息采用清晰的变更类型，中文或英文均可，例如 `新增工作流选择技能`、`docs: refine xxx workflow`。

## 许可证

发布前请在仓库根目录添加许可证文件，明确他人可以如何使用、修改和分发这些技能。
