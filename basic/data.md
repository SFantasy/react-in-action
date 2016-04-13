# 数据流

本节将介绍如何在 React 中应用简单的数据流。

在 React 中，数据的载体主要有两种方式：

- `props`
- `state`

来看一下如何使用者两种不同的方式来处理数据。

## Props

`props` 即属性 (property)

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
