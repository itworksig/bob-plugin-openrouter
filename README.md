# Bob OpenRouter

[itworksig](https://github.com/itworksig) 维护的 [Bob](https://bobtranslate.com/) 翻译插件，通过 [OpenRouter](https://openrouter.ai/) 调用大语言模型翻译。

这是 [helloChenLei/bob-plugin-openrouter](https://github.com/helloChenLei/bob-plugin-openrouter) 的 fork。本仓库的安装包、更新源和后续改动都在这里。

## 本 fork 的改动

- 新增乌兹别克语、塔吉克语、波斯语、哈萨克语、乌尔都语、印尼语、马来语、旁遮普语、普什图语
- 可在「翻译模式」和「自定义 Prompt」之间切换
- 译文按 Markdown 返回，Bob 1.21 及以上会渲染标题、列表和表格
- 插件图标换成 OpenRouter 标志
- 更新检查指向本仓库的 [Releases](https://github.com/itworksig/bob-plugin-openrouter/releases)

## 安装

1. 下载最新插件：[bob-plugin-openrouter.bobplugin](https://github.com/itworksig/bob-plugin-openrouter/releases/latest/download/bob-plugin-openrouter.bobplugin)
2. 双击安装
3. 打开 Bob 偏好设置 → 服务 → OpenRouter，填入 API Key

需要指定版本时，从 [Releases](https://github.com/itworksig/bob-plugin-openrouter/releases) 下载对应的 `.bobplugin`。

## 配置

1. 在 [OpenRouter API Keys](https://openrouter.ai/keys) 创建 API Key
2. 在 Bob 里找到 OpenRouter 服务，填写：

| 选项 | 说明 |
| --- | --- |
| API Key | OpenRouter 的密钥 |
| API Base URL | 固定为 `https://openrouter.ai/api/v1` |
| AI Model | 预设模型，或选「自定义模型」后填写完整模型 ID，例如 `anthropic/claude-3-opus` |
| Prompt 模式 | 「翻译模式」使用内置提示词；「自定义模式」使用自己的 Prompt |

自定义 Prompt 里可以用：

- `{from}`：源语言
- `{to}`：目标语言
- `{text}`：原文。写了它，整段 Prompt 会作为用户消息；没写时，Prompt 作为系统提示，原文单独发送

默认自定义 Prompt：

```text
你是一个翻译助手。请把用户文本翻译成{to}，只返回译文，不要解释。
```

## 支持的语言

简体中文、繁体中文、英语、日语、韩语、法语、德语、西班牙语、意大利语、俄语、葡萄牙语、荷兰语、波兰语、阿拉伯语、南非语、印地语、泰语、越南语、乌兹别克语、塔吉克语、波斯语、哈萨克语、乌尔都语、印尼语、马来语、旁遮普语、普什图语，以及自动检测。

## 预设模型

- GPT-3.5 Turbo `openai/gpt-3.5-turbo`
- GPT-4 `openai/gpt-4`
- Claude 2.1 `anthropic/claude-2.1`
- Claude 3 Opus `anthropic/claude-3-opus`
- Claude 3 Sonnet `anthropic/claude-3-sonnet`
- Gemini Pro `google/gemini-pro`
- Mixtral 8x7B `mistralai/mixtral-8x7b`
- Llama 2 70B `meta-llama/llama-2-70b-chat`
- Code Llama 34B `codellama/codellama-34b-instruct`
- Qwen 72B `qwen/qwen-72b-chat`

其他模型用「自定义模型」填写 OpenRouter 模型 ID。

## 更新日志

### v0.1.12

- 新增乌尔都语、印尼语、马来语、旁遮普语、普什图语

### v0.1.11

- 译文以 Markdown 返回，支持标题、列表和表格

### v0.1.10

- 支持翻译模式和自定义 Prompt

### v0.1.9

- 更换为 OpenRouter 图标

### v0.1.8

- 新增乌兹别克语、塔吉克语、波斯语、哈萨克语

v0.1.7 及更早版本来自上游仓库。

## 相关链接

- 本仓库：https://github.com/itworksig/bob-plugin-openrouter
- 上游：https://github.com/helloChenLei/bob-plugin-openrouter
- Bob：https://bobtranslate.com/
- OpenRouter：https://openrouter.ai/
