# 组件生命周期

React 组件在实例化之后就开始了它的生命周期过程。

在使用组件以及`state`和`props`变化的时候会触发不同的生命周期方法。

以下是一个组件从开始到结束所调用的生命周期方法：

- `getDefaultProps`
- `getInitialState`
- `componentWillMount`
- `render`
- `componentDidMount`
- `componentWillReceiveProps`
- `shouldComponentUpdate`
- `componentWillUpdate`
- `componentDidUpdate`

对于每个方法的详细说明可以参考官方文档：http://facebook.github.io/react/docs/component-specs.html

值得注意的是，由于 React 组件的生命周期方法实际上是一个类似「状态机」的存在，因此在`render`方法中不能调用`this.setState({})`方法 -- 否则就会无限调用`render`方法让程序陷入「崩溃」的状态。
