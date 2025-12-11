# Frontend Sandbox

<div align="center">
  <h3>🎨 一个基于 Vite 的多框架前端实验沙盒</h3>
  <p>快速创建和预览 React、Vue 等各种 UI 组件和交互效果</p>
</div>

## ✨ 特性

- 🚀 **极速启动** - 基于 Vite，毫秒级热更新
- 🎯 **多框架支持** - 内置 React 和 Vue 支持，开箱即用
- 📦 **零配置** - 自动扫描沙盒目录，无需手动配置路由
- 🔥 **即时预览** - 修改代码实时看到效果
- 🎨 **独立沙盒** - 每个实验相互隔离，互不影响
- 📝 **TypeScript 支持** - 完整的类型支持

## 📖 使用说明

每个实验放到 `sandboxs/<name>/` 文件夹下，通过 `/<name>` 路由即可访问。

## 🚀 快速开始

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

服务器将在 `http://localhost:8030` 启动，并自动打开浏览器。

### 创建新实验

在 `sandboxs/` 下创建新文件夹，支持以下方式：

#### 方式 1：纯 HTML/CSS/JS

```bash
mkdir sandboxs/my-demo
echo '<h1>Hello World</h1>' > sandboxs/my-demo/index.html
```

访问：`http://localhost:8030/my-demo`

#### 方式 2：React 组件

创建 `sandboxs/my-react/index.tsx`：

```tsx
import React from 'react';
import ReactDOM from 'react-dom/client';

function App() {
  return <div>Hello React!</div>;
}

ReactDOM.createRoot(document.getElementById('root')!).render(<App />);
```

配套创建 `sandboxs/my-react/index.html`：

```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8" />
    <title>My React Demo</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="./index.tsx"></script>
  </body>
</html>
```

#### 方式 3：Vue 组件

创建 `sandboxs/my-vue/index.vue` 和 `sandboxs/my-vue/__entry.ts`（参考 `sandboxs/vueTest`）

## 📜 可用命令

| 命令 | 说明 |
|------|------|
| `npm run dev` | 启动开发服务器（支持热更新） |
| `npm run build` | 构建生产版本到 `dist/` 目录 |
| `npm run preview` | 预览构建后的生产版本 |

## 📂 项目结构

```
frontend-sandbox/
├── sandboxs/              # 所有实验沙盒
│   ├── demo/             # 纯 HTML 示例
│   ├── reactTest/        # React 示例
│   └── vueTest/          # Vue 示例
├── index.html            # 首页（自动列出所有沙盒）
├── vite.config.js        # Vite 配置
└── package.json
```

## 🎯 内置示例

- **demo** - 纯 HTML/CSS/JS 示例
- **reactTest** - React 组件示例
- **vueTest** - Vue 组件示例

## 💡 技术栈

- ⚡️ [Vite 5](https://vitejs.dev/) - 下一代前端工具
- ⚛️ [React 19](https://react.dev/) - 用于构建用户界面
- 🖖 [Vue 3](https://vuejs.org/) - 渐进式 JavaScript 框架
- 📘 [TypeScript](https://www.typescriptlang.org/) - JavaScript 的超集

## 📝 License

MIT
