# 5.1 CoAP 示例

Contiki 中的 CoAP 是基于低功耗 REST 引擎Erbium（Er）实现的。REST 引擎包含完整的嵌入式 CoAP 的实现，并成为 Contiki 官方引擎之一。

关于 Erbium 实现和作者的详细信息请参阅 [Erbium官方网站](http://people.inf.ethz.ch/mkovatsc/erbium.php) 。

> ## 什么是 REST 和CoAP ?
>
> 表述性状态传递\(Representational State Transfer，REST\)依赖于无状态，客户/服务器模型，可缓存的通信协议，应用场景类似于Http 协议。 RESTful Web服务的关键抽象目标是资源，而不是服务。常见的传感器，执行器和控制系统等都可以优雅地表示为资源，对应的的服务则通过RESTful Web服务暴露给接口。 RESTful应用使用类似HTTP的请求发布数据（创建或更新），读取数据（比如进行查询）以及删除数据。因此，REST可使用HTTP的四个CRUD（创建/读取/更新/删除）操作。 尽管简单，REST功能强大，几乎所有Web服务都可以采用RESTful架构来实现。
>
> 受约束应用协议（COAP）是旨在简化电子设备与互联网交互通信。特别针对小型，低功耗传感器，开关，阀门等需要通过标准Internet网络远程监控的设备。 COAP是一个主要用于资源有限的互联网设备比如WSN节点的应用层协议。
>
> COAP通过简化Web集成能够轻松转换成HTTP，同时也能满足特殊要求，如支持组播，低开销，应用方便。 CoAP can run on most devices that support UDP. CoAP makes use of two message types, requests and responses, using a simple binary base header format. The base header may be followed by options in an optimized Type-Length-Value format. CoAP is by default bound to UDP and optionally to DTLS \(Datagram Transport Layer Security\), providing a high level of communications security.
>
> Any bytes after the headers in the packet are considered the message body \(if any is present\). The length of the message body is implied by the datagram length. When bound to UDP the entire message MUST fit within a single datagram. When used with 6LoWPAN as defined in RFC 4944, messages should fit into a single IEEE 802.15.4 frame to minimize fragmentation.

