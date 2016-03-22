# JSX

关于[JSX](https://github.com/facebook/jsx)，其实很多人乍一看会觉得这是一种技术的退步。

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
