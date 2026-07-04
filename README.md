# PocketStack Skill

## 简介

本 Skill 为 Agent 提供完整的 [PocketStack](https://github.com/citywill/pocket-stack) 开发参考，涵盖模块创建、后端操作、前端风格、路由菜单配置和测试流程。

PocketStack 是基于 **React + PocketBase** 的 AI 友好的全栈模块化开发框架。

## 安装

1. 下载最新版本的压缩包 [pocketstack-skill](https://github.com/citywill/pocketstack-skill/archive/refs/heads/master.zip)
2. 解压到Agent或项目的skills目录（例如`~/.trae-cn/skills/pocketstack-skill/`）

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
