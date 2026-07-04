# 快速开始：安装、初始化项目开发环境

PocketStack 项目的安装和启动流程。

## 1. 克隆项目

```bash
git clone https://github.com/citywill/pocket-stack <项目目录名>
cd <项目目录名>
```

> 项目目录名由用户指定，若用户未提供则默认为 `pocket-stack`。

## 2. 创建环境变量配置文件

```bash
cp .env.example .env
```

## 3. 下载 PocketBase

将 PocketBase 可执行文件下载到项目根目录：

- 前往 [PocketBase Releases](https://github.com/pocketbase/pocketbase/releases) 下载对应平台的可执行文件
- Windows: `pocketbase.exe`
- macOS/Linux: `pocketbase`

将下载的文件放置在项目根目录 `.pocketbase/` 下。

## 4. 安装依赖

```bash
npm install
# 或使用 pnpm
pnpm install
```

## 5. 启动开发环境

```bash
npm run dev
# 或使用 pnpm
pnpm dev
```

该命令会同时启动 PocketBase 后端和 Vite 前端开发服务器。

## 6. 初始化 PocketBase 超级管理员

使用 cli 定义 pocketbase 的 superuser ：
- email：`admin@example.com`
- password：`admin12345`

例如：

```bash
.pocketbase/pocketbase superuser upsert admin@example.com admin12345
```
