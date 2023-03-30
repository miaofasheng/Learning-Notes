# Paper-sharing
此仓库为在实验室组会上论文分享后，撰写的推送稿子


1. **【论文分享】QUICforge: 基于 QUIC 协议的客户端伪造请求攻击**<br />
这篇论⽂是针对 QUIC（Quick UDP Internet Connection）协议发起客⼾端请求伪造攻击，该⼯作由柏林⼯业⼤学分布式基础设施安全实验室的 Yuri Gbur 和 Florian Tschorsch 共同完成。作者从QUIC 协议的设计出发，分析了 (1) 服务端初始请求伪造（Server Initial Request Forgery, SIRF），(2) 版本协商请求伪造 （Version Negotiation Request Forgery, VNRF) 以及 (3) 连接迁移请求伪造（Connection Migration Request Forgery, CMRF ) 这三种典型的客⼾端请求伪造攻击模式。作者发现 VNRF 可⽤于模拟 DNS 等基于 UDP 的协议，SIRF 和 CMRF 可⽤于流量放⼤攻击。作者评估了 13 种开源的 QUIC 协议实现探索了请求伪造攻击的影响，结果表明，所有实现都受 SIRF 和 VNRF 请求伪造攻击影响，QUIC 协议存在潜在的脆弱性。<br />
论⽂发表于国际⽹络安全四⼤顶级学术会议 NDSS 2023。  
<br />

2. **【论文分享】窥探递归解析器的ECS行为**<br />
内容交付网络（Content Delivery Networks，CDN）通常使用 DNS（Domain Name System）将用户映射到最佳边缘服务器。ECS（EDNS0 Client Subnet Extension）扩展允许递归解析器在DNS查询中包含用户子网信息，以便权威域名服务器可以使用这些信息来改进用户映射。
论文从DNS解析服务、DNS解析的交互过程以及权威域名服务器出发，通过分析支持ECS的递归解析器的解析行为，发现一系列有悖协议规范的错误，以及即使符合协议规范，但仍会引入安全风险的有害行为，这些行为可能会侵犯用户隐私，降低DNS缓存的有效性。甚至在某些错误配置的情况下，ECS会降低权威域名服务器优化用户到边缘服务器映射的能力。
<br />论文第一作者来自美国凯斯西储大学，发表于2019年网络测量领域国际顶级会议ACM IMC（录用率：39/197=20%）
