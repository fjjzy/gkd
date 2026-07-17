# GKD-Plus

[简体中文](#zh-cn) | [English](#en)

<a id="zh-cn"></a>

## 简体中文

GKD-Plus 是基于 [GKD](https://github.com/gkd-kit/gkd) 的增强版本，在原版基础上新增 AI 智能规则生成等实用功能。

原作者不希望在上游维护过多扩展功能，因此本项目作为独立分支继续开发更多增强能力。

如果模型规则生成失败，请在应用内进入 `设置 - 关于 - 导出日志`，将日志发送到 `3329221986@qq.com`，或在 GitHub 提交 issue。

### 新增功能

#### AI 智能规则生成

- 支持接入大模型（OpenAI / Anthropic 协议）自动生成点击规则
- 配置灵活：可自定义 API 地址、模型、温度等参数
- 请求队列机制：多次快照不会丢失，按顺序依次处理
- 推荐使用 Deepseek-v4-flash

#### 加强模式（双击快照按钮触发）

- 双击悬浮球触发加强验证流程
- 自动生成规则 → 执行动作 → 验证效果 → 失败自动重试
- 对比执行前后节点树变化，判断规则是否生效
- 最多重试 2 次，重试时携带失败上下文供 AI 参考

#### AI 配置备份/恢复

- 大模型配置（API URL、Key、模型等）纳入备份/导入体系

### 原版功能

GKD 是一个基于 [高级选择器](https://gkd.li/guide/selector)、[订阅规则](https://gkd.li/guide/subscription) 和 [快照审查](https://github.com/gkd-kit/inspect) 的自定义屏幕点击 Android 应用。

- **快捷操作**：简化重复流程，如自动确认电脑登录
- **跳过流程**：自动跳过启动时的烦人流程

### 免责声明

本项目遵循 [GPL-3.0](/LICENSE) 协议。

本项目是 GKD 的独立增强分支，不代表原项目官方立场。如需了解原版 GKD，请访问 [gkd-kit/gkd](https://github.com/gkd-kit/gkd)。

[Back to top](#gkd-plus)

<a id="en"></a>

## English

GKD-Plus is an enhanced fork of [GKD](https://github.com/gkd-kit/gkd), adding practical features such as AI-powered rule generation on top of the original app.

Because the upstream author does not plan to maintain too many extra features in the original project, this repository continues those enhancements as an independent fork.

If AI rule generation fails, open `Settings - About - Export logs` in the app and send the exported logs to `3329221986@qq.com`, or file an issue on GitHub.

### Added Features

#### AI Rule Generation

- Supports large model providers compatible with OpenAI / Anthropic protocols to generate click rules automatically
- Flexible configuration: custom API URL, model, temperature, and related parameters
- Request queue: multiple snapshots are processed in order without being dropped
- Recommended model: Deepseek-v4-flash

#### Enhanced Mode (Triggered by Double-Tapping the Snapshot Button)

- Double-tap the floating button to start an enhanced validation flow
- Generate rule → execute action → verify result → retry automatically on failure
- Compare the node tree before and after execution to determine whether the rule works
- Retry up to 2 times and include failure context for the AI model during retries

#### AI Configuration Backup and Restore

- Large model settings, including API URL, API key, and model name, are included in backup/import flows

### Original GKD Features

GKD is a custom Android screen-clicking app based on [advanced selectors](https://gkd.li/guide/selector), [subscription rules](https://gkd.li/guide/subscription), and [snapshot inspection](https://github.com/gkd-kit/inspect).

- **Quick actions**: simplify repetitive flows, such as confirming desktop login prompts automatically
- **Skip flows**: automatically skip annoying startup flows

### Disclaimer

This project is licensed under [GPL-3.0](/LICENSE).

This project is an independent enhanced fork of GKD and does not represent the official position of the upstream project. For the original GKD project, visit [gkd-kit/gkd](https://github.com/gkd-kit/gkd).

[返回顶部](#gkd-plus)
