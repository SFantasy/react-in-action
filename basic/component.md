# 组件基础

相信「组件化」或者说「模块化」这些词大家都已经耳熟能详了。

由于 JavaScript 本身没有像 Java, Python 等语言一样的模块化方案，因此在 Node.js 大一统之前，前端的世界中曾经出现过各种各样的「组件化」、「模块化」的工具 -- 例如：[require.js](https://github.com/requirejs/requirejs), [sea.js](https://github.com/seajs/seajs) 等。

不过现在就完全可以使用 Node.js 中的模块机制来完成「组件化」、「模块化」的代码组织，而 React 中的组件也是基于这一机制来实现的。

## 定义组件

先来看看如何使用 ES5 或者 ES6 来编写一个 React 的组件。

- ES5

```js
var React = require('react')

var Header = React.createClass({
  render: function () {
    return <header><h1>Title</h1></header>;
  }
})

module.exports = Header;
```

- ES6

```js
import React, { Component } from 'react'

class Header extends Component {
  render () {
    return <header><h1>Title</h1></header>
  }
}

export default Header
```

## 使用组件

组件的使用与其他 Node.js 模块一致，不过在使用的时候是作为自定义标签：

```js
var React = require('react')
var ReactDOM = require('react-dom')

var Header = require('./Header')

ReactDOM.render(
  <Header />,
  document.getElementById('app')
)
```
