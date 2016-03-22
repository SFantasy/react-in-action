# React中的样式

与传统的前端开发相比，使用 React 也有多种定义样式的方式。

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
    color: '#666'
  }
};
```

然后再定义一个组件：

```
var React = require('react');

module.exports = React.createClass({
  render () {
    return <h1 className={styles.title}></h1>
  }
});
```
