代码里 proxyIP 是做什么用的? 原理怎样的? 列的那几个域名安全么? ****.eu.org', '****.cyou 这几个 . [#153](https://github.com/3Kmfi6HP/EDtunnel/issues/153) 

 >  不安全, 除非你自建 zizifn/edgetunnel#162 #123
proxyIP 是一些大厂的ip会转发所有 cf 流量
以前因为worker不让访问cloudflare系的网站，所以客户端->worker->proxyIP->cf网站
现在又加入让 proxyIP 当优选IP(v2ray with bestip), 等于客户端->proxyIP->worker->网站
我刚查了, cdn.xn--b6gac.eu.org 属于 ALIBABA-CN-NET, 也就是你的流量都发给阿里巴巴一遍

[proxyIP 的机器，是如何充当中继节点的呢？ #268](https://github.com/zizifn/edgetunnel/issues/268)
