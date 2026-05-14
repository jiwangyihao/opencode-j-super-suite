# OpenCode J Super Suite

[![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-j-super-suite?style=social)](https://github.com/jiwangyihao/opencode-j-super-suite/stargazers)

OpenCode J Super Suite 是一组 OpenCode 插件的总览仓库，用来帮助用户按需选择、组合和迁移插件。

它不是运行时中心包，也不是共享库。每个插件都可以独立安装、独立发布、独立验证；本仓库只维护能力矩阵、推荐组合、迁移路径、版本兼容关系和示例配置。

## 插件与仓库映射

| 包名 | npm | npm 下载量 | GitHub | Stars |
| --- | --- | --- | --- | --- |
| `opencode-copilot-account-switcher@0.15.0` | [npm](https://www.npmjs.com/package/opencode-copilot-account-switcher) | [![npm downloads](https://img.shields.io/npm/dw/opencode-copilot-account-switcher.svg)](https://www.npmjs.com/package/opencode-copilot-account-switcher) | [jiwangyihao/opencode-copilot-account-switcher](https://github.com/jiwangyihao/opencode-copilot-account-switcher) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-copilot-account-switcher?style=social)](https://github.com/jiwangyihao/opencode-copilot-account-switcher/stargazers) |
| `opencode-openai-account-switcher@0.1.0` | [npm](https://www.npmjs.com/package/opencode-openai-account-switcher) | [![npm downloads](https://img.shields.io/npm/dw/opencode-openai-account-switcher.svg)](https://www.npmjs.com/package/opencode-openai-account-switcher) | [jiwangyihao/opencode-openai-account-switcher](https://github.com/jiwangyihao/opencode-openai-account-switcher) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-openai-account-switcher?style=social)](https://github.com/jiwangyihao/opencode-openai-account-switcher/stargazers) |
| `opencode-loop-safety@0.1.0` | [npm](https://www.npmjs.com/package/opencode-loop-safety) | [![npm downloads](https://img.shields.io/npm/dw/opencode-loop-safety.svg)](https://www.npmjs.com/package/opencode-loop-safety) | [jiwangyihao/opencode-loop-safety](https://github.com/jiwangyihao/opencode-loop-safety) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-loop-safety?style=social)](https://github.com/jiwangyihao/opencode-loop-safety/stargazers) |
| `opencode-wait@0.1.0` | [npm](https://www.npmjs.com/package/opencode-wait) | [![npm downloads](https://img.shields.io/npm/dw/opencode-wait.svg)](https://www.npmjs.com/package/opencode-wait) | [jiwangyihao/opencode-wait](https://github.com/jiwangyihao/opencode-wait) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-wait?style=social)](https://github.com/jiwangyihao/opencode-wait/stargazers) |
| `opencode-notify-tool@0.1.0` | [npm](https://www.npmjs.com/package/opencode-notify-tool) | [![npm downloads](https://img.shields.io/npm/dw/opencode-notify-tool.svg)](https://www.npmjs.com/package/opencode-notify-tool) | [jiwangyihao/opencode-notify-tool](https://github.com/jiwangyihao/opencode-notify-tool) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-notify-tool?style=social)](https://github.com/jiwangyihao/opencode-notify-tool/stargazers) |
| `opencode-oncall@0.1.5` | [npm](https://www.npmjs.com/package/opencode-oncall) | [![npm downloads](https://img.shields.io/npm/dw/opencode-oncall.svg)](https://www.npmjs.com/package/opencode-oncall) | [jiwangyihao/opencode-oncall](https://github.com/jiwangyihao/opencode-oncall) | [![GitHub stars](https://img.shields.io/github/stars/jiwangyihao/opencode-oncall?style=social)](https://github.com/jiwangyihao/opencode-oncall/stargazers) |

## 插件矩阵

| 插件 | 当前版本 | GitHub 仓库 | 主要能力 | 独立性 | 仓库状态 |
| --- | --- | --- | --- | --- | --- |
| `opencode-copilot-account-switcher` | `0.15.0` | [jiwangyihao/opencode-copilot-account-switcher](https://github.com/jiwangyihao/opencode-copilot-account-switcher) | GitHub Copilot 多账号、quota、模型路由、Copilot Network Retry、Copilot status、compact / stop-tool、Synthetic Agent Initiator | 独立 Copilot 领域插件 | GitHub 与 npm 已发布 |
| `opencode-openai-account-switcher` | `0.1.0` | [jiwangyihao/opencode-openai-account-switcher](https://github.com/jiwangyihao/opencode-openai-account-switcher) | OpenAI / Codex 账号切换、Codex status、Codex retry、upstream snapshot | 独立 OpenAI / Codex 领域插件 | GitHub 与 npm 已发布 |
| `opencode-loop-safety` | `0.1.0` | [jiwangyihao/opencode-loop-safety](https://github.com/jiwangyihao/opencode-loop-safety) | Guided Loop Safety 策略注入、`/loop-safety` 菜单、强交互与无人值守等待规则 | 独立策略插件，弱依赖 wait / notify | GitHub 与 npm 已发布 |
| `opencode-wait` | `0.1.0` | [jiwangyihao/opencode-wait](https://github.com/jiwangyihao/opencode-wait) | 通用 `wait` tool，支持固定等待和等待新用户消息 | 完全独立工具插件 | GitHub 与 npm 已发布 |
| `opencode-notify-tool` | `0.1.0` | [jiwangyihao/opencode-notify-tool](https://github.com/jiwangyihao/opencode-notify-tool) | 通用 `notify` tool，提供非阻塞进度通知 | 完全独立工具插件 | GitHub 与 npm 已发布 |
| `opencode-oncall` | `0.1.5` | [jiwangyihao/opencode-oncall](https://github.com/jiwangyihao/opencode-oncall) | 远程值守、微信 slash 指令、通知、`/status`、`/todo`、`/reply`、`/allow`、`/recover`、OpenClaw smoke | 独立远程值守插件 | GitHub 与 npm 已发布 |

## 推荐组合

### 只需要 Copilot 账号切换

```bash
opencode plugin opencode-copilot-account-switcher@0.15.0 --force -g
```

适合只使用 GitHub Copilot provider，希望管理多个 Copilot 账号、查看 quota 或启用 Copilot 专属请求增强的用户。

### 只需要 OpenAI / Codex 账号切换

```bash
opencode plugin opencode-openai-account-switcher@0.1.0 --force -g
```

适合只使用 OpenAI / Codex provider，需要独立账号管理、status 和 retry 的用户。

### 通用 Loop Safety 工作流

```bash
opencode plugin opencode-wait@0.1.0 --force -g
opencode plugin opencode-notify-tool@0.1.0 --force -g
opencode plugin opencode-loop-safety@0.1.0 --force -g
```

适合长任务代理工作流。`wait` 负责无人值守等待，`notify` 负责非阻塞进度通知，`loop-safety` 负责策略注入和交互约束。

### 远程值守 / 微信交互

```bash
opencode plugin opencode-oncall@0.1.5 --force -g
```

适合需要远程值守、通过微信接收通知、处理 slash 指令、查看 `/status` 或使用 `/todo` 恢复待处理事项的用户。

### Copilot + Loop Safety + 远程值守

```bash
opencode plugin opencode-copilot-account-switcher@0.15.0 --force -g
opencode plugin opencode-wait@0.1.0 --force -g
opencode plugin opencode-notify-tool@0.1.0 --force -g
opencode plugin opencode-loop-safety@0.1.0 --force -g
opencode plugin opencode-oncall@0.1.5 --force -g
```

适合需要 Copilot 账号能力、长任务安全策略和远程值守能力的完整组合。

## 迁移路径

如果你曾经只安装 `opencode-copilot-account-switcher`，现在请按实际需求拆分安装：

1. 继续需要 Copilot 账号、quota、routing 或 Copilot Network Retry：保留 `opencode-copilot-account-switcher@0.15.0`。
2. 需要 OpenAI / Codex 账号切换：新增 `opencode-openai-account-switcher@0.1.0`。
3. 需要 Guided Loop Safety：新增 `opencode-wait@0.1.0`、`opencode-notify-tool@0.1.0` 和 `opencode-loop-safety@0.1.0`。
4. 需要远程值守 / 微信交互：新增 `opencode-oncall@0.1.5`。
5. 不要用裸包名或 `latest`；始终使用带明确版本号的安装命令。

## 设计原则

- **独立插件优先：** 每个插件都能单独安装和验证。
- **弱依赖优先：** 组合只增强体验，不让某个插件成为其它插件的运行中心。
- **不预设共享库：** 只有当真实复用稳定且复制成本高于抽库成本时，才考虑共享库。
- **文档先行：** 总览仓库维护选择指南，不替代各插件自己的 README、Release Notes 和发布流程。

## 文档

- [插件兼容表](./docs/compatibility.md)
- [迁移指南](./docs/migration.md)
- [示例配置](./examples/opencode-plugins.md)

## License

MPL-2.0。详见 [LICENSE](./LICENSE)。
