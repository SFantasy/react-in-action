# 学习JSX

[JSX](https://github.com/facebook/jsx) 在 React 中是很重要的一个组成部分，用于展示 DOM 结构与应用中的数据展示。

在前一节中，我们已经见识过 JSX 了:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

其中`render` 方法的第一个参数就是一个 JSX 语法的

## 技术的退步？

关于[JSX](https://github.com/facebook/jsx)，相信很多人跟我一样会觉得这是一种技术的退步。

因为我们以前在进行前端开发的时候，总是会把 HTML、 CSS 和 JavaScript 进行分离 -- 这也是很容易理解的一点，把用户界面中的结构、样式、逻辑分开，便于开发和维护。

但是 JSX 似乎历史的道路上往回走了，以下是 JSX 官方标准中的一个示例：

```
// Using JSX to express UI components.
var dropdown =
  <Dropdown>
    A dropdown list
    <Menu>
      <MenuItem>Do Something</MenuItem>
      <MenuItem>Do Something Fun!</MenuItem>
      <MenuItem>Do Something Else</MenuItem>
    </Menu>
  </Dropdown>;

render(dropdown);
```
