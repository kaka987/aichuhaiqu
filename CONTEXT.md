# 项目上下文 — AI出海去 (aichuhaiqu.com)

## 项目定位
AI出海去是一个面向中国AI创客的出海知识平台，内容涵盖AI工具、海外公司注册、收付款、产品发布、增长/SEO、流量变现、跨境电商等。由莱特卡卡（@litekakacom）创立，LiteStartup 联合创始人。

## 技术架构
- **发布方式**：本地 Markdown + Git + LiteStartup Skills（一句话发布）
- **域名**：aichuhaiqu.com
- **LiteStartup domain_slug**：`domain-9cdc304ab3bd18a98396fd3fba0104f3`
- **Git 仓库**：https://github.com/kaka987/aichuhaiqu.git
- **平台环境**：Windows (PowerShell)，无 bash

## 目录结构
```
├── RULE.md              # AI 执行规则（同步命令、文档规范等）
├── CONTEXT.md           # 本文件，项目上下文
├── litestartup.yaml     # LiteStartup 绑定配置
├── .gitignore           # 排除 assets/ 和 rules/
├── website/
│   ├── index.html       # 首页（杂志/周刊风格，经典黑白）
│   └── about.html       # 关于我们（block 类型，继承 header/footer）
├── docs/
│   ├── config.json      # 文档站配置（主题、links、footer）
│   └── zh/
│       ├── _nav.md      # 顶部导航（一级栏目入口）
│       ├── _sidebar.md  # 首页级侧边栏（栏目目录）
│       ├── index.md     # 文档站首页
│       ├── ai-tools/    # AI工具&技术
│       │   ├── _sidebar.md   # 栏目独立侧边栏
│       │   ├── index.md
│       │   └── coding/       # 子分类：编程工具
│       │       └── cc-switch.md
│       ├── overseas-company/  # 注册海外公司（含独立 _sidebar.md）
│       ├── payment/           # 海外收付款
│       ├── product-launch/    # 产品发布
│       ├── growth/            # 增长&广告&SEO
│       ├── monetization/      # 流量变现
│       └── ecommerce/         # 跨境电商
├── rules/               # 内部撰写规范（gitignore，不提交）
│   └── ai-tools-doc-template.md
└── assets/              # 原始素材存放（gitignore，不提交）
    └── docs/            # 工具 README 等原始资料
```

## 文档导航架构
- **`_nav.md`**（顶栏）→ 一级栏目入口，点击切换栏目
- **各栏目 `_sidebar.md`** → 栏目内独立侧边栏，override 父级
- **子分类目录**（如 `coding/`、`infra/`）→ 按工具用途细分，sidebar 中分组展示

## 内容分类策略
- **知识型内容** → `docs/zh/` （教程、工具介绍、长青内容）
- **时效型内容** → `blog/` （周刊、创客故事、成功案例）— 尚未创建

## 发布流程
1. 本地编写 Markdown / HTML
2. `git push` 到 GitHub
3. 执行 RULE.md 中的同步命令（全量或按需）触发 LiteStartup 发布

## 关键配置
- API Key 位于 `~/.litestartup/credentials`
- docs 主题：黑白极简（primary_color: #111111, dark_mode: true）
- 页面类型：website = 完整独立 HTML, block = 继承父页 header/footer
