# React中的样式

与传统的前端开发一样，使用 React 也有多种定义样式的方式。以下先简单介绍一下几种比较常见的方式：

## 行内样式

React 中定义行内样式的方式和传统的 HTML 中不一样，例如：

```
<p style={{ color: '#0f0' }}>Inline Styling</p>
```

我们需要传递一个包含样式属性的对象到标签的`style`属性中。

## 样式与组件的分离

一般在 Web 开发的时候我们会要求将 HTML 与 CSS 进行分离，在开发 React 的时候也是一样。

例如，我们可以先写一个样式对象：

```
var styles = {
  title: {
    color: '#666',
    backgroundColor: '#fff'
  }
};
```

然后再定义一个组件：

```js
var React = require('react');

module.exports = React.createClass({
  render () {
    return <h1 style={styles.title}>Title</h1>
  }
});
```

### 使用样式文件

上面提到的方式都是通过 JavaScript 来定义样式，然后应用到 JSX 代码中。

当然也可以通过引入 CSS 文件添加到页面之中，然后通过 DOM 属性进行应用：

```js
var React = require('react');

module.exports = React.createClass({
  render () {
    return <h1 className="title">Title</h1>
  }
});
```

> 机智的你一定注意到了上面代码中的`className`与`backgroundColor`，这和我们平时书写的`class`与`background-color`不同；你可以带着这个问题继续阅读，当然也可以直接去参考[JSX](../jsx/README.md)章节中的内容。
