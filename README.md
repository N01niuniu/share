---
title: share
date: 2017-09-20 10:23:56
tags: [团队分享]
---

## Why prettier ？
统一团队的代码格式

> It is generally accepted that having a common style guide is valuable for a project and team but getting there is a very painful and unrewarding process. People get very emotional around particular ways of writing code and nobody likes spending time writing and receiving nits.

```js
prettier --single-quote --no-semi --write "*.{js,css}"
prettier --config .prettierrc --write "*.{js,css}"
```

<b>和 ESLint 的区别：</b>
Formatting rules
Code-quality rules

prettier 只负责 Formatting rules

结合 husky 和 lint-staged 使用：

```js
"scripts": {
  "precommit": "lint-staged"
},
  "lint-staged": {
  "*.js": ["eslint", "git add"],
  "*.{js,css,scss}": ["prettier --write", "git add"]
}
```

Live Demo：
演示 husky 和 lint-staged

##  nodejs 调试

环境需求：
- node 7+
- chrome 60+ 

```js
node --inspect index.js
node --inspect-brk index.js
```

打开调试面板方式：

- chrome://inspect
- DevTool

调试 .bin 目录：

```js
node --inspect-brk node_modules/.bin/webpack 
```

Live Demo：
调试 hlj 后台 yarn dist:webpack 命令后报错问题

[doc](https://nodejs.org/dist/latest-v8.x/docs/api/debugger.html#debugger_v8_inspector_integration_for_node_js)

## Snippets generator

[在线地址](https://pawelgrzybek.com/snippet-generator/)

## Command Line Tools（cli）

常见的 CLI 项目生成工具：
- create-react-app
- vue-cli
- angular-cli

开发 CLI 常用库：
[commander.js](https://github.com/tj/commander.js)
[Inquirer.js](https://github.com/SBoudrias/Inquirer.js)

Live Demo：
以 react_antd 工程为例，写一个简易的脚手架，用于创建一个基于 SearchBar 和 Table 的模块模版

## Transform.now.sh

[transform.now.sh](https://transform.now.sh/)
