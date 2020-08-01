# 简易RPC框架 Self-RPC

项目架构：Netty + Kyro + Zookeeper 

项目描述：从0实现RPC框架，实现了RPC框架的远程调用，序列化、负载均衡的功能，项目目前还在维护中 

项目演进： 

1、服务发现：支持zookeeper注册中心 

2、通信方式：使用Netty代替BIO实现了网络传输 

3、序列化：使用开源的序列化机制Kyro代替了JDK自带的序列化机制 

4、负载均衡：客户端远程调用服务的时候采用了随机负载均衡算法，还将逐步实现轮询、加权轮询、最小连接等算法【因为涉及到每个节点的性能获取，暂时还没有相关思路】

设计及优化思路： https://blog.nowcoder.net/n/8aa40d4651ea4e5880c5a606c3067a3f



### 各模块的代码解读

| 工具              | 设计思想                                                     |
| ----------------- | ------------------------------------------------------------ |
| 远程通信Netty     | <https://blog.nowcoder.net/n/9494e37e14954ff9909eb0f06da580ac> |
| 序列化Kyro        | <https://blog.nowcoder.net/n/8b62c25bd5354b3d9b79ca10cda991ee> |
| 注册中心zookeeper | <https://blog.nowcoder.net/n/6419ec79f3d045d0a9d20edc83bdc097> |
|                   |                                                              |

