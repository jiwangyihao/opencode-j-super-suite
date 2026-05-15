# 插件兼容表

本表记录已经明确验证或已发布的插件组合。版本号必须写死，避免用户误装 `latest` 后得到不可复现的组合。

## 当前基线

| 组合 | 版本 | 状态 | 说明 |
| --- | --- | --- | --- |
| Copilot 单插件 | `opencode-copilot-account-switcher@1.0.0` | 已发布 | [GitHub](https://github.com/jiwangyihao/opencode-copilot-account-switcher) / [npm](https://www.npmjs.com/package/opencode-copilot-account-switcher)；Copilot 账号、quota、routing、retry 与 status 聚合在一个包内。 |
| OpenAI / Codex 单插件 | `opencode-openai-account-switcher@0.1.0` | 已发布 | [GitHub](https://github.com/jiwangyihao/opencode-openai-account-switcher) / [npm](https://www.npmjs.com/package/opencode-openai-account-switcher)；不依赖 Copilot 包。 |
| Loop Safety 完整组合 | `opencode-wait@0.1.0` + `opencode-notify-tool@0.1.0` + `opencode-loop-safety@0.1.0` | 已发布 | [GitHub](https://github.com/jiwangyihao/opencode-loop-safety) / [npm](https://www.npmjs.com/package/opencode-loop-safety)；`loop-safety` 弱依赖 wait / notify；缺失工具时应降级。 |
| 远程值守 / 微信交互 | `opencode-oncall@0.1.5` | 已发布 | [GitHub](https://github.com/jiwangyihao/opencode-oncall) / [npm](https://www.npmjs.com/package/opencode-oncall)；远程值守、微信 slash 指令、通知、`/status`、`/todo`、`/reply`、`/allow`、`/recover`。 |
| Skill 去重 / 上下文精简 | `opencode-skill-deduper@0.1.4` | 已发布 | [GitHub](https://github.com/jiwangyihao/opencode-skill-deduper) / [npm](https://www.npmjs.com/package/opencode-skill-deduper)；压缩旧的重复 skill 正文，保留最新 skill 指令，并通过文件日志和 TUI notifier 记录真实压缩事件。 |
| Copilot + 远程值守 | `opencode-copilot-account-switcher@1.0.0` + `opencode-oncall@0.1.5` | 推荐组合 | 两者不应通过内部模块互相依赖。 |
| Copilot + Loop Safety 完整组合 | `opencode-copilot-account-switcher@1.0.0` + wait / notify / loop-safety 当前基线 | 推荐组合 | Copilot 包不再拥有 Loop Safety 运行时代码。 |
| 全量 Super Suite 组合 | Copilot / OpenAI / wait / notify / loop-safety / oncall / skill-deduper 当前基线 | 推荐组合 | `opencode-skill-deduper` 不依赖其它插件，可与账号、等待、通知和远程值守插件并行安装。 |

## 兼容性规则

1. 独立插件不能依赖 `opencode-j-super-suite`。
2. 总览仓库只记录推荐组合，不替代插件自己的发布链路。
3. 每次更新矩阵时，必须写明具体版本号和验证状态。
4. 如果某个组合只是设计目标但尚未验证，状态必须写成「待验证」。
