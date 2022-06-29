---
sidebar_position: 2
---

# 2、HTML中的JavaScript

## `<script>`元素

`<script>`元素有下列8个属性：
- async：可选。表示应该立即开始下载脚本，但不能阻止其他页面动作，比如下载资源或等待其他脚本加载。只对外部脚本文件有效。
- charset：可选。使用src属性指定的代码字符集。
- crossorigin：可选。配置相关请求的 CORS（跨源资源共享）设置。默认不使用 CORS。 crossorigin="anonymous"配置文件请求不必设置凭据标志。 crossorigin="use-credentials"设置凭据标志，意味着出站请求会包含凭据。
- defer：可选。表示脚本可以延迟到文档完全被解析和显示之后再执行。
- integrity：可选。允许比对接收到的资源和指定的加密签名以验证子资源完整性（ SRI，Subresource Integrity）。如果接收到的资源的签名与这个属性指定的签名不匹配，则页面会报错，脚本不会执行。这个属性可以用于确保内容分发网络（ CDN， Content Delivery Network）不会提供恶意内容。
- language：废弃。
- src：可选。表示包含要执行的代码的外部文件。
- type：可选。表示代码块中脚本语言的内容类型（也称 MIME 类型）。

> 使用了 src 属性的`<script>`元素不应该再在`<script>`和`</script>`标签中再包含其他JavaScript 代码。如果两者都提供的话，则浏览器只会下载并执行脚本文件，从而忽略行内代码。

### defer 与 async

async与defer类似，都只适用于外部脚本，都会告诉浏览器立即下载。不过，与defer不同的是，标记为async的脚本并不保证能按照他们出现的顺序执行。

## 文档模式

最初文档模式有两种：**混杂模式**和**标准模式**

## `<noscript>`元素

`<noscript>`元素用于给不支持javascript的浏览器提供替代内容。

```html
<!DOCTYPE html>
<html>
  <head>
  <title>Example HTML Page</title>
  <script defer="defer" src="example1.js"></script>
  <script defer="defer" src="example2.js"></script>
  </head>
  <body>
  <noscript>
    <p>This page requires a JavaScript-enabled browser.</p>
  </noscript>
  </body>
</html>

```