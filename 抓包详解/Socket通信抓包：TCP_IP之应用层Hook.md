Socket通信抓包：TCP/IP之应用层Hook

- Socket的本质：收发包的接口（单位的传达室）、高速公路、一条通道，跑的都是 RAW DATA, 纯 Binary
- Socket本质上不是中间人抓包，本质就是一个网卡流量dump
- TCP/IP之应用层：HTTP + SSL 、 ProtoBuf + SSL
- 转储的内容已经不是Socket，而是SSL的接口（关键）
- HOOK SSL框架直接得到明文
- SSL Framework中有哪些有趣的API
- HOOK native层直接得到明文
- ssl logger源码解析