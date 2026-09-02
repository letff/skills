# Personal Codex Skills

个人维护的可复用 Codex 技能集合。每个技能是独立目录，包含必需的 `SKILL.md`，并可按需带有 `agents/`、`scripts/`、`references/` 或 `assets/`。

## 当前技能

| 技能 | 用途 |
| --- | --- |
| `document-driven-development` | 按快速、标准或复杂档，以方案、进度、调整和成果文档驱动代码改动。 |

## 目录结构

```text
.
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

## 维护约定

- 每项技能保持独立目录和唯一的 `name`。
- 共享前删除令牌、内部地址、客户数据和个人绝对路径。
- 修改技能时更新对应的 `SKILL.md`；涉及桌面界面元数据时同步更新 `agents/openai.yaml`。
- 提交信息采用清晰的变更类型，例如 `feat: add xxx skill`、`docs: refine xxx workflow`。

## 许可证

发布前请在仓库根目录添加许可证文件，明确他人可以如何使用、修改和分发这些技能。
