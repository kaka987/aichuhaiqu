---
title: CC Switch — AI 编程工具统一管理神器
description: 一个桌面应用管理 Claude Code、Codex、Gemini CLI 等 7 款 AI 编程工具，50+ 供应商预设一键切换，告别手动编辑配置文件
date: 2025-06-17
tags: [coding, config-management, cross-platform]
github_star: 103000
status: recommended
---

# CC Switch — AI 编程工具统一管理神器

> **GitHub Star 103k+ · Fork 6.8k+** · Trendshift 上榜项目
>
> 官网：[ccswitch.io](https://ccswitch.io) · 仓库：[github.com/farion1231/cc-switch](https://github.com/farion1231/cc-switch)

---

## 它解决什么问题？

AI 编程时代，开发者往往同时使用多款 AI 编程工具——Claude Code、Claude Desktop、Codex、Gemini CLI、OpenCode、OpenClaw、Hermes 等。但每款工具都有自己独立的配置格式（JSON / TOML / `.env`），面临以下痛点：

| 痛点 | 具体表现 |
|------|---------|
| **配置碎片化** | 每个工具各有一套 API Key、Base URL、模型参数的配置方式 |
| **切换成本高** | 更换 API 供应商需手动编辑多个配置文件，极易出错 |
| **MCP/Skills 各自为政** | 在不同工具间安装和管理 MCP Server、Skills 无法统一 |
| **缺少用量可视化** | 跨供应商的 Token 消耗、费用支出无法集中追踪 |

---

## CC Switch 是什么？

CC Switch 是一款基于 **Tauri 2 + Rust** 构建的跨平台桌面应用，提供统一的可视化界面来管理所有主流 AI 编程工具。

**一句话概括**：一个应用管 7 个 AI 工具，50+ 供应商预设一键切换。

---

## 核心功能

### 供应商管理

- 支持 **Claude Code、Claude Desktop、Codex、Gemini CLI、OpenCode、OpenClaw、Hermes** 共 7 款工具
- 内置 **50+ 供应商预设**（含 AWS Bedrock、NVIDIA NIM 及社区中转服务）
- 一键切换、系统托盘快速访问、拖拽排序、导入导出
- **通用供应商**模式：一份配置同步到 Claude Code、Codex 和 Gemini CLI

### 统一 MCP / Skills 管理

- 一个面板管理所有工具的 MCP Server，支持双向同步和 Deep Link 导入
- Markdown 编辑器管理 Prompts，跨应用同步 CLAUDE.md / AGENTS.md / GEMINI.md
- Skills 支持从 GitHub 仓库或 ZIP 文件一键安装，自定义仓库管理

### 代理与故障转移

- 本地代理热切换，支持格式转换、自动故障转移、熔断器和健康监控
- 应用级代理接管——可为 Claude、Codex、Gemini 分别配置代理

### 用量与成本追踪

- 跨供应商追踪支出、请求数和 Token 用量
- 趋势图表、详细请求日志和自定义模型定价

### 云同步与系统集成

- 支持 Dropbox、OneDrive、iCloud、坚果云、NAS 及 WebDAV 同步
- Deep Link 协议（`ccswitch://`）一键导入供应商、MCP、提示词和技能
- 深色/浅色/跟随系统主题、开机自启、自动更新

---

## 市场表现

| 指标 | 数据 |
|------|------|
| **GitHub Star** | 103,000+ |
| **Fork** | 6,800+ |
| **支持平台** | Windows / macOS / Linux |
| **支持工具** | 7 款主流 AI 编程工具 |
| **供应商预设** | 50+ |
| **Trendshift** | 上榜热门项目 |
| **许可证** | MIT |

---

## 技术架构

```
前端：React 18 · TypeScript · Vite · TailwindCSS · shadcn/ui
后端：Tauri 2.8 · Rust · SQLite · Tokio
设计：SSOT 单一事实源 · 原子写入 · 双向同步 · 分层架构
```

核心设计亮点：
- **SQLite 单一事实源**：所有供应商、MCP、提示词数据统一存储
- **原子写入**：临时文件 + 重命名模式，防止配置文件被损坏
- **Mutex 并发安全**：保护数据库连接，避免竞态条件

---

## 安装

### Windows

从 [GitHub Releases](https://github.com/farion1231/cc-switch/releases) 下载 `.msi` 安装包或 `.zip` 绿色版。

### macOS（推荐 Homebrew）

```bash
brew install --cask cc-switch
```

### Linux

支持 `.deb`（Debian/Ubuntu）、`.rpm`（Fedora/RHEL）、`.AppImage`（通用）。

---

## 快速开始

1. **添加供应商**：点击"添加供应商" → 选择预设或自定义
2. **切换供应商**：主界面点击"启用"或系统托盘直接点击供应商名称
3. **管理 MCP**：点击"MCP" → 添加服务器 → 切换同步开关
4. **安装 Skills**：点击"Skills" → 浏览 GitHub 仓库 → 一键安装

---

## 适用人群

- 同时使用多款 AI 编程工具的开发者
- 需要在多个 API 供应商间频繁切换的用户
- 希望统一管理 MCP Server 和 Skills 的团队
- 对 AI 编程工具用量和成本有追踪需求的个人或企业

---

## 相关链接

- **官网**：[ccswitch.io](https://ccswitch.io)
- **GitHub**：[github.com/farion1231/cc-switch](https://github.com/farion1231/cc-switch)
- **许可证**：MIT © Jason Young
