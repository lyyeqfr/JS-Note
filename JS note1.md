# 第一章  什么是 JavaScript

## 1.1 JavaScript 实现

  完整的JavaScript实现包含三个部分：

* 核心（ECMAScript）

* 文档对象模型（DOM）

* 浏览器对象模型（BOM）

  ```mermaid
  flowchart LR
    subgraph JavaScript
      ECMAScript
      DOM
      BOM
      end
  ```

###   .1 ECMAScript

  > ECMA-262规范定义的标准化脚本语言，核心功能：语法、类型、语句、关键字、保留字、操作符、全局对象。

​    宿主环境：提供ECMAScript的基准实现和与环境自身交互必需的扩展（Web浏览器只是一种）。 

​    ES6：ECMA-262第6版，也称ES2015，于2015年6月发布，包含这个规范最重要的一批增强特性。

###   .2 DOM

  > 文档对象类型（Document Object Model）是一个应用编程接口（API），用于在HTML中使用扩展的XML。

​    DOM将整个页面抽象为一组分层节点，开发者通过DOM树可以控制网页的内容和结构。

​    为保持Web跨平台的本性，W3C以level级别制定DOM标准。

###   .3 BOM

> 浏览器对象模型，用于支持访问和操作浏览器的窗口。

​    HTML5以正式规范的形式涵盖了尽可能多的BOM特性。





