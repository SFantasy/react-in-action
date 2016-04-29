# 学习JSX

[JSX](https://github.com/facebook/jsx) 在 React 中是很重要的一个组成部分，用于展示 DOM 结构与应用中的数据展示。

在基础部分中，我们已经见识过 JSX 了:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

其中`render` 方法的第一个参数就是一个由 JSX 语法编写的 DOM 结构。

## 技术的退步？

关于[JSX](https://github.com/facebook/jsx)，相信很多人会觉得这是一种技术的退步。

因为我们以前在进行前端开发的时候，总是会把 HTML、 CSS 和 JavaScript 进行分离 -- 这也是很容易理解的一点，把用户界面中的结构、样式、逻辑分开，便于开发和维护。

但是 JSX 似乎在历史的道路上往回走了，不仅给应用带来了一堆 XML 一样的标签，而且将事件与 DOM 结构混合在了一起，例如以下 JSX：

```
<a
  onClick={() => {
    console.log('Click!');
  }}
>Button</>
```

## 为何使用 JSX

JSX 并不是以模板语言的姿态出现在 React 之中的。

在 React 之中，如果没有 JSX，就需要通过另外的方式来创建 Virtual DOM：

```js
React.createElement('h1', { className: 'title' }, 'Title');
```

其实这也是 React 实际工作的代码，虽然这样的代码看起来也不是很繁琐，但是想象一下用这样的方式来构建一个大型的应用呢？

JSX 则是出现改变这种编码方式的解决方案：

```
<h1 className="title">Title</h1>
```

这样既可以让应用的结构变得清晰（主要指的是 DOM 结构）、语义化，又加快了编码的速度和可读性。
