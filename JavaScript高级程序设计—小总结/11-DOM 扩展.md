# DOM 扩展

### 小结：

虽然 DOM 为与 XML 及 HTML 文档交互制定了一系列核心 API，但仍然有几个规范对标准的 DOM
进行了扩展。这些扩展中有很多原来是浏览器专有的，但后来成为了事实标准，于是其他浏览器也都提
供了相同的实现。本章介绍的三个这方面的规范如下。

  Selectors API，定义了两个方法，让开发人员能够基于 CSS 选择符从 DOM中取得元素，这两个
方法是 querySelector() 和 querySelectorAll() 。

  Element Traversal，为 DOM 元素定义了额外的属性，让开发人员能够更方便地从一个元素跳到
另一个元素。之所以会出现这个扩展，是因为浏览器处理 DOM 元素间空白符的方式不一样。

  HTML5，为标准的 DOM 定义了很多扩展功能。其中包括在 innerHTML 属性这样的事实标准基
础上提供的标准定义，以及为管理焦点、设置字符集、滚动页面而规定的扩展 API。

虽然目前 DOM扩展的数量还不多，但随着 Web 技术的发展，相信一定还会涌现出更多扩展来。很
多浏览器都在试验专有的扩展，而这些扩展一旦获得认可，就能成为“伪”标准，甚至会被收录到规范
的更新版本中。