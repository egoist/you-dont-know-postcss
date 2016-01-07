---
title: PostCSS 概览
categories:
  - PostCSS
date: 2016/01/07
---
今天开讲 PostCSS，那就得从 `./index.js` 说起，万事开头简单，`./index.js` 就两行：

```js
require('babel-core/register')({ extensions: ['.es6'] });
module.exports = require('./lib/postcss');
```

什么意思呢？

第一行引入了 babel 的注册器，这样之后 require 的内容都将被 babel 转换为 es5 的格式，而 `extensions` 则指定让 babel 只转换 `.es6` 后缀的文件。

这个 `./index.js` 大概只是开发时用的，开发者在发布新版本的时候会把所有 `.es6` 文件编译成 `es5` 再发布，这样做的好处是开发时免去了编译这一环节，提高效率。

---

好了，今天第一讲很简单，下期再见！

---

Refs:

- [index.js](https://github.com/postcss/postcss/blob/master/index.js)
