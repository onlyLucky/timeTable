<div align="center">
<h1 align="center">vue3-vant-mobile</h1>

An mobile web apps template based on the Vue 3 ecosystem.

一个基于 Vue 3 生态系统的移动 web 应用模板，帮助你快速完成业务开发。

<p>
<img src="https://img.shields.io/github/license/easy-temps/vue3-vant-mobile" alt="license" />
<img src="https://img.shields.io/github/package-json/v/easy-temps/vue3-vant-mobile" alt="version" />
<img src="https://img.shields.io/github/repo-size/easy-temps/vue3-vant-mobile" alt="repo-size" />
<img src="https://img.shields.io/github/languages/top/easy-temps/vue3-vant-mobile" alt="languages" />
<img src="https://img.shields.io/github/issues-closed/easy-temps/vue3-vant-mobile" alt="issues" />
</p>

[文档](https://easy-temps.github.io/easy-docs/vue3-vant-mobile/) / [交流](https://github.com/easy-temps/vue3-vant-mobile/issues/56) / [反馈](https://github.com/easy-temps/vue3-vant-mobile/issues)

<a href="https://vue3-vant-mobile.netlify.app">在线 Demo</a>

[![Netlify Status](https://api.netlify.com/api/v1/badges/e6828bd2-2904-4c3e-a67c-b97d32aa1275/deploy-status)](https://app.netlify.com/sites/vue3-vant-mobile/deploys)

</div>

<br>

## Features

- ⚡️ [Vue 3](https://github.com/vuejs/core), [Vite 5](https://github.com/vitejs/vite), [pnpm](https://pnpm.io/), [esbuild](https://github.com/evanw/esbuild) - 就是快！

- 🗂 [基于文件的路由](./src/router)

- 📦 [组件自动化加载](./src/components)

- 🍍 [使用 Pinia 的状态管理](https://pinia.vuejs.org)

- 📲 [PWA](https://github.com/antfu/vite-plugin-pwa)

- 🎨 [UnoCSS](https://github.com/antfu/unocss) - 高性能且极具灵活性的即时原子化 CSS 引擎

- 🌍 [I18n 国际化开箱即用](./src/locales)

- 🔥 使用 [新的 `<script setup>` 语法](https://github.com/vuejs/rfcs/pull/227)

- 📥 [API 自动加载](https://github.com/antfu/unplugin-auto-import) - 直接使用 Composition API 无需引入

- 💪 TypeScript, 当然

- ⚙️ 使用 [Vitest](https://github.com/vitest-dev/vitest) 进行单元测试

- 💾 [本地数据模拟](https://github.com/pengzhanbo/vite-plugin-mock-dev-server)的支持

- 🌈 Git [hooks](./.husky) - 提交代码 eslint 检测 和 提交规范检测

- 🪶 [Vant](https://github.com/youzan/vant) - 移动端 Vue 组件库

- 🔭 [vConsole](https://github.com/vadxq/vite-plugin-vconsole) - 移动端网页开发工具

- 📱 浏览器适配 - 使用 viewport vw/vh 单位布局

- 💻 [桌面端优化](https://github.com/wswmsword/postcss-mobile-forever) - 处理为移动端视图

- 🌓 支持深色模式

- 🛡️ 将 [ESM](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) 设为默认

- ☁️ 零配置部署 [Netlify](https://www.netlify.com)

<br>

## 预配置

### UI 框架

- [UnoCSS](https://github.com/antfu/unocss) - 高性能且极具灵活性的即时原子化 CSS 引擎
  - [`@unocss/preset-rem-to-px`](https://github.com/unocss/unocss/tree/main/packages/preset-rem-to-px) - 将所有实用程序的 rem 转换为 px
  - [`eslint-plugin-unocss`](https://github.com/devunt/eslint-plugin-unocss) - Unocss 的 ESLint 插件
- [Vant](https://github.com/youzan/vant) - 移动端 Vue 组件库
  - [`vant-touch-emulator`](https://github.com/youzan/vant/tree/main/packages/vant-touch-emulator) - 在桌面端上模拟移动端 touch 事件
  - [`vant-use`](https://github.com/youzan/vant/tree/main/packages/vant-use) - Vant 内置的组合式 API
- [element plus](https://element-plus.org/zh-CN/) - 基于 Vue 3，面向设计师和开发者的组件库

### 插件

- [Vue Router](https://github.com/vuejs/router)
  - [`unplugin-vue-router`](https://github.com/posva/unplugin-vue-router) - 以文件系统为基础的路由
- [Pinia](https://pinia.vuejs.org) - 直接的, 类型安全的, 使用 Composition API 的轻便灵活的 Vue 状态管理库
  - [`pinia-plugin-persistedstate`](https://github.com/prazdevs/pinia-plugin-persistedstate) -  适用于 Pinia 的持久化存储插件
- [Vue I18n](https://github.com/intlify/vue-i18n-next) - 国际化
  - [`unplugin-vue-i18n`](https://github.com/intlify/bundle-tools/tree/main/packages/unplugin-vue-i18n) - Vue I18n 的 Vite 插件
- [unplugin-vue-components](https://github.com/antfu/unplugin-vue-components) - 自动加载组件
- [unplugin-auto-import](https://github.com/antfu/unplugin-auto-import) - 直接使用 Composition API 等，无需导入
- [vite-plugin-vconsole](https://github.com/vadxq/vite-plugin-vconsole) - vConsole 的 vite 插件
- [vite-plugin-mock-dev-server](https://github.com/pengzhanbo/vite-plugin-mock-dev-server) - vite mock 开发服务（mock-dev-server）插件
- [postcss-mobile-forever](https://github.com/wswmsword/postcss-mobile-forever) - 一款 PostCSS 插件，将固定尺寸的移动端视图转为具有最大宽度的可伸缩的移动端视图
- [vite-plugin-vue-devtools](https://github.com/vuejs/devtools-next) - 旨在增强Vue开发者体验的Vite插件
- [vueuse](https://github.com/antfu/vueuse) - 实用的 Composition API 工具合集
- [@unhead/vue](https://github.com/unjs/unhead) - 响应式地操作文档头信息
- [vite-plugin-pwa](https://github.com/antfu/vite-plugin-pwa) - PWA
- [vite-plugin-sitemap](https://github.com/jbaubree/vite-plugin-sitemap) - sitemap 和 robots 生成器

### 编码风格

- 使用 Composition API 地 [`<script setup>` SFC 语法](https://github.com/vuejs/rfcs/pull/227)
- [ESLint](https://eslint.org/) 配置为 [@antfu/eslint-config](https://github.com/antfu/eslint-config), 单引号, 无分号

### 开发工具

- [TypeScript](https://www.typescriptlang.org/)
- [Vitest](https://github.com/vitest-dev/vitest) - 基于 Vite 的单元测试框架
- [pnpm](https://pnpm.js.org/) - 快, 节省磁盘空间的包管理器
- [Netlify](https://www.netlify.com/) - 零配置的部署
- [VS Code Extensions](./.vscode/extensions.json)
  - [Vite](https://marketplace.visualstudio.com/items?itemName=antfu.vite) - 自动启动 Vite 服务器
  - [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) - Vue 3 `<script setup>` IDE 支持
  - [Iconify IntelliSense](https://marketplace.visualstudio.com/items?itemName=antfu.iconify) - 图标内联显示和自动补全
  - [i18n Ally](https://marketplace.visualstudio.com/items?itemName=lokalise.i18n-ally) - 多合一的 I18n 支持
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

## 现在可以试试

> vue3-vant-mobile 需要 Node 版本 18+

### GitHub 模板

[使用这个模板创建仓库](https://github.com/easy-temps/vue3-vant-mobile/generate)

### 克隆到本地

如果您更喜欢使用更干净的 git 历史记录手动执行此操作

```bash
npx tiged easy-temps/vue3-vant-mobile my-mobile-app
cd my-mobile-app
pnpm i # 如果你没装过 pnpm, 可以先运行: npm install -g pnpm
```

## 应用需求

### 20241007

1. 整理代码模版（基础页面，底部菜单，顶部navbar组件可以适当调整）。
2. 首页基础功能
    - 当前日期时间（角标展示总任务，已经结束任务数）
    - 切换时间表模式功能（点击菜单选择）
    - 添加任务入口（跳转新增任务界面）
    - 更多功能（菜单点击）搜索任务，跳转日期，备份，设置。
    - 今天日程任务（当前时间节点的即将要做的事情）
    - 历史今天，左滑右滑可以查看（可以展示图片，点击进入详情）
    - 跳转今天
    - 预留广告位
3. 新增任务日程页面
    - 当前日期时间
    - 切换时间表模式功能
    - 添加任务入口
4. 设置
    - 功能设置 导入（方式）、课程表设置、周期任务设置
    - 提醒设置 任务是否提示、提前多久提示、节日祝福提醒、默认全天提醒时间
    - 其他设置 是否显示农历、是否显示节日、是否显示取消任务、关于我们
5. 优化个性化公共组件（后续）

## 开发日志
### 20241007
1. 调整首页页面多余内容

## 使用

### 开发

只需要执行以下命令就可以在 <http://localhost:3000> 中看到

```bash
pnpm dev
```

### 构建

构建该应用只需要执行以下命令

```bash
pnpm build
```

然后你会看到用于发布的 `dist` 文件夹被生成。

### 部署到 Netlify

前往 [Netlify](https://app.netlify.com/start) 并选择你的仓库, 一路 `OK` 下去，稍等一下后，你的应用将被创建。
