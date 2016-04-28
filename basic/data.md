# 数据流

本节将介绍如何在 React 中应用简单的数据流。

在 React 中，数据的载体主要有两种方式：

- `props`
- `state`

来看一下如何使用者两种不同的方式来处理数据。

## Props

`props` 即属性 (property)，是在组件初始化之后就从父级组件带入的到组件内部。

我们无法在使用的过程中对组件的属性进行修改。

```js
// 定义一个 React 组件
var A = React.createClass({
  render: function () {
    return <h1>{this.props.text}</h1>
  }
})

// 使用组件 A
ReactDOM.render(
  <A text="title" />,
  document.getElementById('app')
)
```

在以上代码中，我们定义了一个组件 A，然后在 `render` 方法中渲染了一个内容为 `this.props.text` 的变量。

## State

`state`则是实际上组件中使用的「数据」：

```js
var B = React.createClass({
  getInitialState: function () {
    return {
      value: 0
    }
  },

  render: function () {
    return (
      <div>
        <input value={this.state.value} />
        <button onClick={() => {
          this.setState({
            value: ++this.state.value
          })
        }}>+</button>
      </div>
    )
  }
})

ReactDOM.render(
  <B />,
  document.getElementById('app')
)
```

在上述例子中，可以看到我们给一个`<button>`绑定了`click`事件：

```js
this.setState({
  value: ++this.state.value
});
```

调用 `this.setState()` 方法可以修改组件的`state`，并重新调用`render`方法 -- 重新渲染组件。
