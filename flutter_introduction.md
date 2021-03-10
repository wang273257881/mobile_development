# Flutter

### 诞生

Flutter是Google在2015年推出的移动UI框架，可以快速在iOS和Android上构建高质量的原生用户界面。

Flutter第一次亮相于2015年5月Dart开发者峰会上，初始名字叫做Sky，后更名为Flutter，Flutter使用Dart语言开发，Dart是Google于2011年推出的新的计算机编程语言。

Flutter可以与现有的代码一起工作，并且Flutter是完全免费、开源的。

### 特点

- #### 快速开发

​        Flutter的热重载可快速地进行测试、构建UI、添加功能并更快地修复错误。在iOS和Android模拟器或真机上可以在亚秒内重载，并且不会丢失状态。    

- #### 富有表现力和灵活的UI

​        Flutter内置Material Design和Cupertino（iOS风格）widget、丰富的motion API、平滑而自然的滑动效果和平台感知，使用户可以实现难以置信的快速渲染和富有表现力、灵活的设计。  

- #### 便捷的开发体验

​        Flutter拥有丰富的工具和库，可以帮助用户轻松地同时在iOS和Android系统中实现想法和创意。   

- #### 跨平台自绘引擎

​        使用自带的高性能渲染引擎（Skia）进行自绘，渲染速度和用户体验堪比原生，不仅可以保证在Android和iOS上UI的一致性，而且也可以避免对原生控件依赖而带来的限制及高昂的维护成本。

### Dart语言

​        Flutter APP采用Dart语言开发。Dart在 JIT模式下，速度与 JavaScript基本持平。但是 Dart支持 AOT，当以 AOT模式运行时，JavaScript便远远追不上了。

- #### **开发效率高**

​        Dart运行时和编译器支持Flutter的两个关键特性的组合：

​        **基于JIT的快速开发周期**：Flutter在开发阶段采用，采用JIT模式，这样就避免了每次改动都要进行编译，极大的节省了开发时间；

​        **基于AOT的发布包**:  Flutter在发布时可以通过AOT生成高效的ARM代码以保证应用性能。而JavaScript则不具有这个能力。

- #### **高性能**

​        Flutter旨在提供流畅、高保真的的UI体验。为了实现这一点，Flutter中需要能够在每个动画帧中运行大量的代码。这意味着需要一种既能提供高性能的语言，而不会出现会丢帧的周期性暂停，而Dart支持AOT，在这一点上可以做的比JavaScript更好。

- #### **快速内存分配**

​        Flutter框架使用函数式流，这使得它在很大程度上依赖于底层的内存分配器。因此，拥有一个能够有效地处理琐碎任务的内存分配器将显得十分重要，在缺乏此功能的语言中，Flutter将无法有效地工作。当然Chrome  V8的JavaScript引擎在内存分配上也已经做的很好，事实上Dart开发团队的很多成员都是来自Chrome团队的，所以在内存分配上Dart并不能作为超越JavaScript的优势，而对于Flutter来说，它需要这样的特性，而Dart也正好满足而已。

- #### **类型安全**

​        由于Dart是类型安全的语言，支持静态类型检测，所以可以在编译前发现一些类型的错误，并排除潜在问题，这一点对于前端开发者来说可能会更具有吸引力。与之不同的，JavaScript是一个弱类型语言，也因此前端社区出现了很多给JavaScript代码添加静态类型检测的扩展语言和工具，如：微软的TypeScript以及Facebook的Flow。相比之下，Dart本身就支持静态类型，这是它的一个重要优势。

### 框架

![Flutter框架](https://upload-images.jianshu.io/upload_images/14594750-75a45d1b52ca12a0.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

如上图所示为Flutter官方给出的系统架构图，可以看出Flutter框架分为三层：Framework层、Engine层和Embedder层。

- #### Framework层

  ​        由Dart来实现，包含众多安卓Material风格和iOS Cupertino风格的Widgets小部件，还有渲染、动画、绘图和手势等。Framework包含日常开发所需要的大量API，普通应用开发熟悉这些API的使用基本OK了，不过很多特殊场景的控件需要自己根据实际情况进行自定义。

- #### Engine层

  ​        由C/C++实现，是Flutter的核心引擎，主要包括Skia图形引擎、Dart运行时环境Dart VM、Text文本渲染引擎等。

- #### Embedder层

  ​        主要处理一些平台相关的操作，如渲染Surface设置、本地插件、打包、线程设置等。