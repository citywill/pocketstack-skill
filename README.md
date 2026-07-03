# PocketStack Skill

## 简介

[PocketStack](https://github.com/citywill/pocket-stack) 是基于 **React + shadcn/ui + PocketBase** 的全栈模块化开发框架。本 Skill 为 AI 编程助手提供完整的开发参考，涵盖模块创建、后端操作、前端风格、路由菜单配置和测试流程。

## 目录结构

```
pocketstack-skill/
├── SKILL.md                     # Skill 入口（工作流程、关键约定、文件位置）
├── README.md                    # 本文件
└── references/                  # 详细参考文档
    ├── initialization.md        # 快速开始：安装、初始化项目开发环境
    ├── module.md                # 模块结构：目录规范、文件命名、CRUD 模板
    ├── frontend.md              # 前端风格：组件库、图标、主题色、布局
    ├── routing.md               # 路由与菜单：路由定义、权限控制、菜单配置
    ├── backend.md               # 后端开发：PocketBase CRUD、过滤语法、Collection 创建
    ├── testing.md               # 测试流程：编译测试、浏览器测试、测试账号
    └── example.md               # 开发示例：examples 模块页面索引
```

## 工作流程

开发一个功能模块遵循以下步骤：

1. **创建模块** — 按照模块结构创建目录和文件
2. **后端** — 通过 PocketBase MCP 创建 collection
3. **前端页面** — 参考 examples 实现页面和组件
4. **路由和菜单** — 配置 `routes.tsx` 和 `menu.ts`（自动注册，无需手动导入主文件）
5. **测试** — 编译测试 + Chrome DevTools 浏览器测试

## 关键约定

| 类别 | 约定 |
|------|------|
| 模块目录命名 | kebab-case（`finance`、`notebooklm`） |
| 页面文件命名 | 大驼峰 PascalCase |
| 页面访问路径 | `/{module}/{page}` |
| Collection 命名 | `{module}_subPageName` |
| UI 组件 | shadcn/ui，通过 MCP 添加，禁止手写新组件 |
| 图标 | `@heroicons/react/24/outline` |
| 主题色 | 使用 CSS 变量 `primary`，禁止硬编码颜色 |
| 表单 | `react-hook-form` |
| 国际化 | 纯中文 |
| TypeScript | 严格模式，禁用 `any`（除非必要需注释） |
| 路由/菜单 | 自动从 modules 目录导入，无需手动注册 |

## 技术栈

- **构建工具**：Vite 7、pnpm workspaces
- **前端**：React 19、React Router 7、TypeScript 5.9、Tailwind CSS v4
- **UI**：shadcn/ui（Maia 风格）、Radix UI
- **后端/数据**：PocketBase（SDK 0.26）
- **表单**：react-hook-form
- **工具**：date-fns、sonner、tailwind-merge、clsx

## 快速开始

```bash
# 1. 克隆项目
git clone https://github.com/citywill/pocket-stack
cd pocket-stack

# 2. 下载 PocketBase 可执行文件到 .pocketbase/ 目录
# 3. 安装依赖
pnpm install

# 4. 启动开发（同时启动 PocketBase 和 Vite）
pnpm dev
```

## 参考文档说明

| 文档 | 内容 |
|------|------|
| `initialization.md` | 项目安装和启动流程 |
| `module.md` | 模块目录结构、文件命名规范、CRUD 模板示例 |
| `frontend.md` | 前端技术栈、主题色规则、图标使用、布局组件 |
| `routing.md` | 路由定义、权限控制组件、菜单项配置 |
| `backend.md` | PocketBase 客户端、CRUD 操作、过滤语法、Collection 创建 |
| `testing.md` | 编译测试命令、浏览器测试步骤、测试账号 |
| `example.md` | examples 模块页面索引 |
