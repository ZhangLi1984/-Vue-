```markdown
# 用Vue打造微信小程序，让你的开发效率翻倍！
**日期：** 2023-06-27  
**阅读时间：** 3分钟  
**阅读量：** 5,540  
**专栏：** 微信小程序

Vue作为当前最流行的前端框架之一，以其轻量级的JavaScript框架特性，在开发效率、易用性和灵活性等方面表现出色。

## Vue的优势应用于微信小程序
- **更快的开发速度**：Vue的模板语法简单易学，开发者可快速上手。
- **更好的可维护性**：组件化架构使代码结构更加清晰，易于维护。
- **跨平台支持**：支持Web、移动端、桌面应用等多个领域。

## Vue在微信小程序中的应用
在微信小程序中使用Vue框架，需要借助第三方库。目前比较流行的有mpvue和uni-app。本文重点介绍uni-app，作为一款基于Vue的跨平台框架，它支持同时开发多个平台（包括微信小程序、H5、App等），使用同一套代码即可完成多个平台的开发，提供了大量的组件和API，便于快速开发跨平台应用。

### 一套代码多个平台
uni-app支持同时开发多个平台（如微信小程序、H5、App等），使用同一套代码即可完成多个平台的开发。

### 脚手架搭建框架和开发环境
确保已安装Node.js，接下来安装vue-cli：
```bash
npm install -g vite
```
创建uni-app使用Vue3/Vite版：
```bash
npx degit dcloudio/uni-preset-vue#vite my-vue3-project
cd my-vue3-project
npm i
```

### 运行调试
提前下载好微信小程序开发工具：
```bash
npm run dev:weixin
```
运行方式：打开微信开发者工具，导入`dist\dev\mp-weixin`运行。

### 打包编译
执行以下命令：
```bash
npm run build:mp-weixin
```
更多命令请查看`package.json`。

### 需要注意的点
- **请求**：需要HTTPS，在本地可用HTTP（需勾选不校验合法域名），但上传时只能用HTTPS。
- **JavaScript引入**：动态引入方式不支持，无法使用script标签。
- **CSS长度单位**：请使用rpx。
```
