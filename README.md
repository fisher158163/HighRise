# HighRise

喜欢Google Flutter的理由

![Google Flutter](https://ws3.sinaimg.cn/large/006tKfTcgy1ft4l8lykprj318g0gawfg.jpg)

在 [Google I/O ’17](https://www.youtube.com/watch?v=w2TcYP8qiRI) 上，Google 向我们介绍了 Flutter —— 一款新的用于创建移动应用的开源库。

正如你所想的那样，Flutter 是能够帮助创建拥有漂亮 UI 界面的跨平台移动应用解决方案。Flutter 的界面设计与 web 应用类似，因此，你能够从 Flutter 上找到像使用 HTML/CSS 那样熟悉的感觉。

Google 表示：
> Flutter 将会帮你更容易，更快速的开发出界面美观的移动应用。

听起来很美好，但是首先要说的是，我对其他跨平台解决方案，诸如  Xamarin，PhoneGap，Ionic，React Native 等并不是很认可。 大家都知道，这些解决方案互有利弊，很难选择。虽然我并不确定 Flutter 是否会与它们有所不同，但是我很期待。

Flutter 在 Android 前端开发上具有[很多特色](https://flutter.io/technical-overview/)，很有吸引力。这篇文章，我将会告诉你们我之所以喜欢 Flutter 的真正原因，我们现在就开始吧！

**为什么要用 Flutter **

你可能会好奇，然后问自己一个问题：

> Flutter 有什么创新之处？它是如何工作的？与 React Native 有什么不同之处？

我不会在这里讨论技术问题，因为其他人做得更好。如果你对 Flutter 的工作细节感兴趣，我建议你读读这篇文章：[Flutter 的革命性创新是什么？](https://medium.com/m/global-identity?redirectUrl=https://hackernoon.com/whats-revolutionary-about-flutter-946915b09514)你也可以在“ [The Magic of Flutter](https://docs.google.com/presentation/d/1B3p0kP6NV_XMOimRV09Ms75ymIjU5gr6GGIX74Om_DE/edit) ”演示中查看 Flutter 概念的总结。

简要来说，Flutter 是一个移动 SDK ，允许我们创建混合移动应用（这样你就可以编写一份代码，在 Android 和 iOS 都可以运行这个应用程序）。你在 Dart 中编写代码，这是一种由谷歌开发的语言，如果你以前用过 Java ，那看它会觉得非常熟悉。你不再需要用 XML 文件构建布局树，而是像这样：

```
import 'package:flutter/material.dart';

class HelloFlutter extends StatelessWidget {  @override
  Widget build(BuildContext context) {    return new MaterialApp(
      title: "HelloFlutter",
      home: new Scaffold(
        appBar: new AppBar(
          title: new Text("HelloFlutter"),
        ),
        body: new Container(
          child: new RaisedButton(onPressed: _handleOnPressed),
        ),
      ),
    );
  }
}

```

正如你所看到的，布局是由嵌套的组件（小部件）构建的。核心部件是 MaterialApp（这是整个应用程序），然后我们有了 Scaffold （这是主要的布局结构），然后在里面我们有 AppBar（像 Android 工具栏）和一些容器作为主体。在内部，我们将放置布局小部件 —— 文本、按钮等。

简介到此为止。如果你想了解更多关于布局的内容，请查看 [关于 Flutter 构建布局的教程](https://flutter.io/tutorials/layout/)。

#### 1.热重载

好的，现在就开始吧！

我们从一个基本的应用开始。我们有三个按钮，它们中的每一个都能改变文本的颜色：

