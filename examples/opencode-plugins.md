# 示例配置

这些示例只展示推荐安装组合。实际是否写入全局或项目级配置，取决于你使用 OpenCode 的方式。

## 最小 Copilot 组合

```bash
opencode plugin opencode-copilot-account-switcher@0.15.0 --force -g
```

## 长任务代理组合

```bash
opencode plugin opencode-wait@0.1.0 --force -g
opencode plugin opencode-notify-tool@0.1.0 --force -g
opencode plugin opencode-loop-safety@0.1.0 --force -g
```

## 远程微信组合

```bash
opencode plugin opencode-wechat@0.1.1 --force -g
```

## 全量推荐组合

```bash
opencode plugin opencode-copilot-account-switcher@0.15.0 --force -g
opencode plugin opencode-openai-account-switcher@0.1.0 --force -g
opencode plugin opencode-wait@0.1.0 --force -g
opencode plugin opencode-notify-tool@0.1.0 --force -g
opencode plugin opencode-loop-safety@0.1.0 --force -g
opencode plugin opencode-wechat@0.1.1 --force -g
```