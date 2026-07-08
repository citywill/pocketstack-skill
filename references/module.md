# 模块结构

## 目录结构

```
src/modules/{module}/
├── components/           # 模块专用组件
│   └── XxxDrawer.tsx     # 抽屉、对话框等组件
├── migrations/           # PocketBase collection 迁移文件
│   └── {module}.json
├── {subModule}/          # 子模块（可选）
│   ├── components/
│   │   ├── XxxFormDrawer.tsx
│   │   └── XxxDetailDrawer.tsx
│   ├── migrations/
│   │   └── {module}_xxx.json   # PocketBase collection schema
│   ├── Index.tsx
│   └── types.ts
├── PageName.tsx          # 页面文件（大驼峰命名）
├── menu.ts               # 菜单配置（必须导出 menu）
├── routes.tsx            # 路由配置（必须导出 routes）
├── types.ts              # 类型定义
├── package.json          # 模块描述
└── README.md             # 模块说明文档
```

## 文件命名

- 页面文件：大驼峰（PascalCase），如 `ListPage.tsx`, `AdminPage.tsx`
- 组件文件：大驼峰，如 `PostFormDrawer.tsx`
- 类型文件：小驼峰，如 `types.ts`

## 页面访问路径

页面访问路径格式：`/{module}/{page}`

例如：
- 模块 `craftor` 的 `CollectionList` 页面 → `/craftor/collection-list`
- 模块 `examples` 的 `Dashboard` 页面 → `/examples/dashboard`

## 模块 README.md

每个模块建议在根目录放置一个 `README.md` 文件，用于说明模块的功能、结构和用途，便于 AI Agent 和开发者快速理解模块。

```markdown
# {模块名称}

## 模块概述
简要描述模块的核心功能和业务场景。

## 功能特性
- 特性1：说明
- 特性2：说明

## 数据模型
- {module}_xxx - collection 说明
```

## 参考示例

完整的 CRUD 示例位于 `src/modules/examples/curd/`，包含：
- 表格列表页 + 分页/搜索/过滤/排序
- 抽屉表单（创建/编辑）
- 抽屉详情（查看）
- 删除确认弹窗
- PocketBase collection 操作

其他示例：
- 仪表盘：`src/modules/examples/Dashboard.tsx`
- 表格：`src/modules/examples/Table.tsx`
- 表单：`src/modules/examples/Form.tsx`
- AI 对话：`src/modules/examples/AiChat.tsx`
- 落地页（游客访问）：`src/modules/examples/LandingPage.tsx`
