# Ajax 与 Comet

### 小结：

Ajax 是无需刷新页面就能够从服务器取得数据的一种方法。关于 Ajax，可以从以下几方面来总结
一下。

  负责 Ajax 运作的核心对象是 XMLHttpRequest （XHR）对象。

  XHR 对象由微软最早在 IE5 中引入，用于通过 JavaScript 从服务器取得 XML 数据。

  在此之后，Firefox、Safari、Chrome 和 Opera 都实现了相同的特性，使 XHR 成为了 Web 的一个
事实标准。

  虽然实现之间存在差异，但 XHR 对象的基本用法在不同浏览器间还是相对规范的，因此可以放
心地用在 Web 开发当中。

同源策略是对 XHR 的一个主要约束，它为通信设置了“相同的域、相同的端口、相同的协议”这一
限制。试图访问上述限制之外的资源，都会引发安全错误，除非采用被认可的跨域解决方案。这个解决
方案叫做 CORS（Cross-Origin Resource Sharing，跨源资源共享），IE8 通过 XDomainRequest 对象支持
CORS，其他浏览器通过 XHR 对象原生支持 CORS。图像 Ping 和 JSONP 是另外两种跨域通信的技术，
但不如 CORS 稳妥。

Comet 是对 Ajax 的进一步扩展，让服务器几乎能够实时地向客户端推送数据。实现 Comet 的手段
主要有两个：长轮询和 HTTP 流。所有浏览器都支持长轮询，而只有部分浏览器原生支持 HTTP 流。SSE
（Server-Sent Events，服务器发送事件）是一种实现 Comet 交互的浏览器 API，既支持长轮询，也支持
HTTP 流。

Web Sockets是一种与服务器进行全双工、双向通信的信道。与其他方案不同，Web Sockets 不使用
HTTP 协议，而使用一种自定义的协议。这种协议专门为快速传输小数据设计。虽然要求使用不同的
Web 服务器，但却具有速度上的优势。
各方面对 Ajax 和 Comet 的鼓吹吸引了越来越多的开发人员学习 JavaScript，人们对 Web 开发的关注
也再度升温。与 Ajax 有关的概念都还相对比较新，这些概念会随着时间推移继续发展。