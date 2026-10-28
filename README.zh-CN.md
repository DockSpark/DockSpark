# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

DockSpark 让你直接从 macOS 程序坞切换浏览器配置文件。将鼠标悬停在受支持的浏览器图标上，即可选择所需配置文件，无需打开浏览器的配置文件菜单。

[下载最新版本](https://github.com/DockSpark/DockSpark/releases/latest)
· [官方网站](https://dockspark.app)
· [更新日志（英文）](CHANGELOG.md)
· [反馈问题](https://github.com/DockSpark/DockSpark/issues)

## 功能

- 从浏览器程序坞图标旁的弹出面板切换配置文件
- 使用原生 macOS 应用管理浏览器配置文件
- 自定义名称和颜色，快速识别配置文件
- 选择在程序坞悬停菜单中显示哪些命名配置文件
- 使用 DockSpark Free，或通过 Pro 解锁无限数量的浏览器和配置文件
- 显示或隐藏菜单栏图标和程序坞图标
- 在应用内检查更新
- 从“帮助”菜单打开文档或发送结构化反馈
- 支持英语、简体中文、繁体中文、日语、韩语、德语、法语和西班牙语
- 悬停面板随程序坞图标大小缩放，支持程序坞放大效果
- 可在“通用”设置中关闭匿名使用情况分析

## 系统要求

- macOS 14.0 或更高版本
- Apple 芯片或 Intel Mac
- 将受支持的浏览器保留在程序坞中

### 支持的浏览器

| 浏览器 | 程序坞配置文件切换 |
| --- | --- |
| Safari | 支持 |
| Firefox | 支持 |
| Google Chrome | 支持 |
| Chromium | 支持 |
| Microsoft Edge | 支持 |
| Brave Browser | 支持 |
| Vivaldi | 支持 |
| Opera | 支持 |
| Opera GX | 支持 |
| Arc | 支持 |

已安装的 Safari、Google Chrome 和 Firefox 默认启用。Free 方案允许启用一个浏览器，每个浏览器最多三个命名配置文件；无痕浏览和隐身模式入口不计入此限制。Pro 可解除这些限制。你可以从应用列表中添加其他已安装的浏览器。

## 安装

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### 手动下载

1. 打开[最新版本页面](https://github.com/DockSpark/DockSpark/releases/latest)。
2. 下载 `DockSpark-0.5.0.dmg`。请勿下载 GitHub 自动生成的源代码压缩包。
3. 打开磁盘映像，将 `DockSpark.app` 拖入“应用程序”文件夹。
4. 启动 DockSpark，并授予所请求的 macOS 权限。

也可以下载 `DockSpark-0.5.0.zip` 手动安装。

DockSpark 已使用 Developer ID 证书签名，并通过 Apple 公证。

## 权限

DockSpark 仅请求切换配置文件所需的系统权限：

- **辅助功能**：检测鼠标指针与程序坞中受支持浏览器图标的交互。
- **自动化**：允许 DockSpark 请求所选浏览器切换配置文件。
- **完全磁盘访问权限**：可选权限，仅用于发现 Chromium 和 Firefox 的配置文件元数据。

你可以随时在**系统设置 > 隐私与安全性**中查看或撤销这些权限。

## 使用方法

1. 将受支持的浏览器添加到程序坞。
2. 在 DockSpark 中配置浏览器及其配置文件。
3. 将鼠标悬停在该浏览器的程序坞图标上。
4. 从弹出面板中选择配置文件。

## AI 助手技能

[DockSpark 技能](skills/dockspark/SKILL.md)可帮助 AI 助手介绍 DockSpark 的用途和适用场景，指导安装和日常使用，查找官方文档，以及排查常见问题。技能版本 **0.5.0** 与应用版本保持一致；随附指南已对照 DockSpark 0.5.0 核查。助手会使用你的语言回答。

通过 [Skills CLI](https://github.com/vercel-labs/skills) 安装（需要 Node.js；当前环境要求请参阅其文档）：

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

按提示选择你的 AI 助手。默认安装到当前项目，添加 `-g` 可全局安装。上述 GitHub 命令要求技能已发布到本仓库。从本地检出目录安装时，使用：

```sh
npx skills add . --skill dockspark
```

若要[手动安装到 Codex](https://developers.openai.com/codex/skills/)，请将整个 `skills/dockspark` 目录（包括 `references/` 和 `agents/`）复制到 `~/.agents/skills/dockspark`，或项目内的 `.agents/skills/dockspark`。其他助手可能使用不同的技能目录。如果技能未显示，请重新加载助手的技能或开启新会话。

示例提示词：

- `使用 $dockspark 介绍 DockSpark 能帮我做什么。`
- `使用 $dockspark 帮我配置 Chrome 配置文件。`
- `使用 $dockspark 排查为什么鼠标悬停在程序坞图标上没有反应。`

你也可以用英语或其他语言提问。技能提供使用指导；要使用应用，仍需单独安装 DockSpark。每次发布新应用版本时，应核查技能指南和官方链接，并同步更新技能版本及核查基准版本。

## 截图

![DockSpark 配置文件管理窗口](Assets/img_dockspark.jpg)

> 截图展示了 DockSpark 的界面。0.5.0 版本支持从程序坞切换 Safari、Firefox、Chrome 以及上表所列其他 Chromium 内核浏览器的配置文件。

## 更新

DockSpark 使用 Sparkle 提供应用内更新。你也可以从[发布页面](https://github.com/DockSpark/DockSpark/releases)手动下载版本。

## 发布文件完整性

SHA-256 校验值如下：

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

下载后可运行以下命令验证：

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## 反馈

请通过 [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) 报告问题或提出改进建议。报告问题时，请附上 macOS 版本、浏览器版本和复现步骤。

本仓库包含 DockSpark 的公开发布资料，不包含应用源代码。
