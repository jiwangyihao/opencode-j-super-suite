# 迁移指南

## 从单体 Copilot 插件迁移

旧的 `opencode-copilot-account-switcher` 曾经承载多类能力。拆分后，Copilot 包只保留 Copilot 领域功能，其它能力迁移到独立插件。

### 能力对应表

| 旧能力 | 新归属 | 安装命令 |
| --- | --- | --- |
| GitHub Copilot 账号、quota、routing、retry、status | `opencode-copilot-account-switcher` | `opencode plugin opencode-copilot-account-switcher@1.0.0 --force -g` |
| OpenAI / Codex 账号切换、Codex status / retry | `opencode-openai-account-switcher` | `opencode plugin opencode-openai-account-switcher@0.1.0 --force -g` |
| Guided Loop Safety | `opencode-loop-safety` | `opencode plugin opencode-loop-safety@0.1.0 --force -g` |
| `wait` tool | `opencode-wait` | `opencode plugin opencode-wait@0.1.0 --force -g` |
| `notify` tool | `opencode-notify-tool` | `opencode plugin opencode-notify-tool@0.1.0 --force -g` |
| 远程值守 / 微信交互 | `opencode-oncall` | `opencode plugin opencode-oncall@0.1.5 --force -g` |
| 重复 skill 正文压缩 / 上下文去重 | `opencode-skill-deduper` | `opencode plugin opencode-skill-deduper@0.1.4 --force -g` |

## 推荐迁移步骤

1. 先升级 Copilot 包到 `opencode-copilot-account-switcher@1.0.0`。
2. 根据你实际使用的能力，逐个安装独立插件。
3. 重启正在运行的 OpenCode 实例。
4. 如果长会话里反复加载 Superpowers、OmO skills 或 slash command，可额外安装 `opencode-skill-deduper@0.1.4`。
5. 用各插件自己的主入口验证：
   - Copilot：`opencode auth login --provider github-copilot`
   - OpenAI / Codex：对应插件 README 中的 OpenAI / Codex 账号入口
   - Loop Safety：`/loop-safety`
   - 远程值守 / 微信交互：微信侧 `/status`
   - Skill 去重：重复加载同一个长 skill 后查看 `~/.config/opencode/logs/skill-deduper/daily/` 日志
6. 如果 OpenCode 仍加载旧插件缓存，先清理对应缓存目录，再重新执行带版本号的安装命令。

## 注意事项

- 不要安装 `latest`，也不要让 LLM 自行猜包名。
- 不要把 `opencode-j-super-suite` 当成要安装的运行时插件。
- 如果某个插件的 GitHub Release 正文给出更新版本，以该插件 Release 的明确版本号为准。
