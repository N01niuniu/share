---
title: share
date: 2017-09-20 10:23:56
tags: [团队分享]
---

## 为什么使用 Prettier ？

[Prettier](https://github.com/prettier/prettier) 是一个代码格式化工具，可用语统一团队的代码格式

简单的命令行使用：
```js
prettier --single-quote --no-semi --write "*.{js,css}"
prettier --config .prettierrc --write "*.{js,css}"
```

<b>和 ESLint 的区别：</b>
prettier 只负责代码格式部分，不涉及到代码质量部分

结合 [husky](https://github.com/typicode/husky) 和 [lint-staged](https://github.com/okonet/lint-staged) 使用：

```js
"scripts": {
  "precommit": "lint-staged"
},
  "lint-staged": {
  "*.js": ["eslint", "git add"],
  "*.{js,css,scss}": ["prettier --write", "git add"]
}
```

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

[doc](https://nodejs.org/dist/latest-v8.x/docs/api/debugger.html#debugger_v8_inspector_integration_for_node_js)

## Snippets generator

[在线地址](https://pawelgrzybek.com/snippet-generator/)

## Command Line Tools（cli）

常见的 CLI 项目生成工具：
- create-react-app
- vue-cli
- angular-cli

开发 CLI 常用库：
- [commander.js](https://github.com/tj/commander.js)
- [Inquirer.js](https://github.com/SBoudrias/Inquirer.js)

## Transform.now.sh

[transform.now.sh](https://transform.now.sh/)
