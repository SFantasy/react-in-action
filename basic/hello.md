# Hello React

> Talk is cheap, show me the code.

废话就不多说了，从常规的 Hello World 程序开始学习 React 吧！

以下是[官方文档](http://facebook.github.io/react/docs/getting-started.html)中的第一个 React 程序:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Hello React!</title>
    <script src="build/react.js"></script>
    <script src="build/react-dom.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.23/browser.min.js"></script>
  </head>
  <body>
    <div id="example"></div>
    <script type="text/babel">
      ReactDOM.render(
        <h1>Hello, world!</h1>,
        document.getElementById('example')
      );
    </script>
  </body>
</html>
```

以上代码通过`ReactDOM`这个对象，创建了一个`<h1>`元素，并将其插入到了id为 example 的`div`之中。

这里我们使用的是一种名为[JSX]()的语法，即在 JavaScript 中使用类似 HTML 的代码用以展示程序的结构。
