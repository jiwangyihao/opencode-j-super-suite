# 插件兼容表

本表记录已经明确验证或已发布的插件组合。版本号必须写死，避免用户误装 `latest` 后得到不可复现的组合。

## 当前基线

| 组合 | 版本 | 状态 | 说明 |
| --- | --- | --- | --- |
| Copilot 单插件 | `opencode-copilot-account-switcher@0.15.0` | 已发布 | Copilot 账号、quota、routing、retry 与 status 聚合在一个包内。 |
| OpenAI / Codex 单插件 | `opencode-openai-account-switcher@0.1.0` | 已发布 | 不依赖 Copilot 包。 |
| Loop Safety 完整组合 | `opencode-wait@0.1.0` + `opencode-notify-tool@0.1.0` + `opencode-loop-safety@0.1.0` | 已发布 | `loop-safety` 弱依赖 wait / notify；缺失工具时应降级。 |
| 微信远程交互 | `opencode-wechat@0.1.1` | npm 已发布 | GitHub 远端待补齐；当前按 npm 版本记录。 |
| Copilot + 微信 | `opencode-copilot-account-switcher@0.15.0` + `opencode-wechat@0.1.1` | 推荐组合 | 两者不应通过内部模块互相依赖。 |
| Copilot + Loop Safety 完整组合 | `opencode-copilot-account-switcher@0.15.0` + wait / notify / loop-safety 当前基线 | 推荐组合 | Copilot 包不再拥有 Loop Safety 运行时代码。 |

## 兼容性规则

1. 独立插件不能依赖 `opencode-j-super-suite`。
2. 总览仓库只记录推荐组合，不替代插件自己的发布链路。
3. 每次更新矩阵时，必须写明具体版本号和验证状态。
4. 如果某个组合只是设计目标但尚未验证，状态必须写成「待验证」。