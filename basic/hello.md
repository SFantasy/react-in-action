# Hello React

相信所有的编程教程都会从Hello World的例子开始，我们也不例外，就从此开始学习吧！

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

嗯，你可以将上述代码直接复制黏贴到你喜欢的编辑器中，保存之后直接在浏览器中打开这个 HTML 文件就可以看到代码的效果了。

## 这段代码做了什么

首先，我们引入了`react.js`, `react-dom.js` 以及一个托管在Cloudflare CDN 上的 babel-core 的在浏览器中运行的版本。

然后，以上代码通过`ReactDOM`这个对象的`render`方法，创建了一个`<h1>`元素，并将其插入到了id为 example 的`div`之中。

这里我们使用的是一种名为[JSX](https://github.com/facebook/jsx)的语法，这在下一节[JSX](../jsx/README.md) 中会比较详细的讲解。简单来说，JSX 就是在 JavaScript 中使用类似 XML 的代码用以展示DOM 的结构。
