# 第二章  HTML中的JavaScript

## 2.1 \<script>元素

> 将JavaScript插入HTML的主要方法，后被正式加入HTML规范。

 **在\<script>元素中的代码被计算完成之前，页面的其余内容不会被加载和被显示。**

 使用方式：

1. 嵌入JavaScript代码，

   > 使用反斜杠“\”来向文本字符串添加特殊字符。

2. 包含外部JavaScript文件。

   > 使用src属性，属性值URL指向包含JavaScript代码的文件。
   

  可以是一个完整的URL指向来自外部域的资源。浏览器发送GET请求获取资源，并当成加载页面的一部分解释，这样可以通过不同的域分发JavaScript，但要**确保是可信的来源**。

  注意：两种方式同时使用，浏览器只会下载并执行脚本文件，而忽略行内代码。

###   .1 标签位置

  过去外部的CSS和JavaScript被集中放到页面的\<head>标签内。浏览器把所有JavaScript代码下载、解析和解释完成后才开始渲染。期间浏览器窗口完全空白。

  现代Web应用程序通常将所有JavaScript引用放在\<body>元素中的页面内容后面，浏览器显示空白页面的时间变短，用户感觉页面加载更快。

###   .2 推迟执行脚本

> defer属性，表示脚本执行不改变页面结构（立即下载延迟执行，只对外部文件有效）。

###   .3 异步执行脚本

> async属性，不同于defer不保证脚本按照出现次序执行，目的告诉浏览器不必等待。

###   .4 动态加载脚本

通过向DOM中动态添加script元素加载指定脚本（默认异步，统一行为设置同步）。获取的资源对浏览器预加载器不可见，严重影响性能，改进在文档头部显式声明。

### .5 XHTML中的变化

> 可扩展超文本标记语言XHTML是将HTML作为XML的应用重新包装结果。

 在XHTML中与HTML的不同：

1. 使用JavaScript必须指定 type=text/javascript ，
2. 使用\<script>元素嵌入JavaScript代码失效，
3. 解析\<script>元素不会应用特殊规则。

##  2.2 行内代码与外部文件

 将JavaScript代码放在外部文件中通常被认为最佳实践，理由：

1. 可维护性：用一个目录保存所有JavaScript文件更容易维护。

2. 缓存：浏览器设置缓存所有JavaScript文件，用到同一文件只需下载一次。

3. 适应未来：兼容XHTML。

> 在SPDY/HTTP2中，预请求的消耗显著降低，以轻量、独立JavaScript组件形式送达脚本更具优势。


## 2.3 文档模式

 使用doctype切换文档模式

类型：

1. 混杂模式：让IE支持一些非标准的特性，
2. 标准模式：让IE具有兼容标准的行为，

> 准标准模式：支持很多标准特性，没有那么严格（与标准非常接近，很少需要区分）。

## 2.4 \<noscript>元素

> 用于给早期不支持JavaScript的浏览器提供替代内容，显示包含在\<noscript>中的内容。

