---
sidebar_position: 1
---

# JavaScript实现

完整的JavaScript实现包含以下几个部分：
- 核心（ECMAScript）
- 文档对象模型（DOM）
- 浏览器对象模型（BOM）

ECMAScript即ECMA-262定义的语音，并不局限于Web浏览器。事实上，这门语音没有输入和输出之类的方法。

在基本的层面，ECMA-262描述这门语音的如下部分：
- 语法
- 类型
- 语句
- 关键字
- 保留字
- 操作符
- 全局对象

## DOM

文档对象模型是一个应用编程接口（API），用于在HTML中使用扩展的XML。
DOM将整个页面抽象成为一组分层节点。

1998年10月，DOM Level 1 成为W3C的推荐标准。该规范由两个模块组成：DOM Core和DOM HTML。
前者提供了一种映射XML文档，从而方便访问和操作文档任意部分的方式；后者扩展了前者，并增加了特定于HTML的对象和方法。

DOM Level 2对最初DOM的扩展增加了对（DHTML早就支持的）鼠标和用户界面事件、范围、遍历（迭代DOM节点的方法）的支持，而且通过对象接口支持了层叠样式表（CSS）
DOM Level 2新增了以下模块：
- DOM视图
- DOM事件
- DOM样式
- DOM遍历和范围

DOM Level 3进一步扩展了DOM，增加了以统一的方式**加载和保存文档的方法（包含在一个叫DOM Load and Save的新模块中）**，还有**验证文档的方法（DOM Validation）**。

## BOM

使用 BOM，开发者可以操控浏览器显示页面之外的部分。而 BOM 真正独一无二的地方，当然也是问题最多的地方，就是它是唯一一个没有相关标准的 JavaScript 实现。

HTML5 改变了这个局面，这个版本的 HTML 以正式规范的形式涵盖了尽可能多的 BOM 特性。