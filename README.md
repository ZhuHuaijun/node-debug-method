Node调试方法有很多种，在网上可以查到很多（参考 [调试 - 入门指南 | Node.js](https://nodejs.org/zh-cn/docs/guides/debugging-getting-started/)）。本文仅分享自己最常用的Chrome调试方法。

#启用检查器

可以使用 --inspect 参数来启动检查器。但是这样代码不会停止执行，所以通常使用 --inspect-brk 参数来在用户代码启动前终止，从而利于调试代码。

新建文件test.js，随意输入一段代码：

```
  let a = 1;
  let b = 2;
  let c = a + b;

  console.log(c);
```

在文件目录下运行命令：`node --inspect-brk test.js`

#使用chrome调试工具调试

2、打开chrome浏览器，在url中输入 `chrome://inspect`，然后会看到如下界面。

![img](img.png)

点击inspect开始调试。

![img2](img2.png)

现在就可以通过chrome调试工具进行调试了。