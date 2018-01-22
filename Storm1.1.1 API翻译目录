---
title: Storm1.1.1 API翻译目录
tags: Storm1.1.1,翻译
grammar_cjkRuby: true
---

## 中文文档

----------
注意

在最新版本中，类包路径已经从"backtype.storm"改为"org.apache.storm" ，所以如果topology基于旧（0.10.2及以前）的版本编译，无法在Storm1.0.0以后的版本中运行。通过以下配置可以实现向下兼容
**client.jartransformer.class: "org.apache.storm.hack.StormShadeTransformer"**
如果想将编译的代码在旧版本storm上运行，你需要将以上配置添加到storm中。这些配置必须添加到你要提交运行topologies的机器上去。

详细信息请参考：[https://issues.apache.org/jira/browse/STORM-1202](https://issues.apache.org/jira/browse/STORM-1202)

### Storm基础
* Javadoc
* (Concepts) 概念
* (Scheduler) 调度程序
* (Configuration) 配置 
* 消息保证机制
* 容错机制
* 命令窗口
* REST API
* 理解Storm topology并行化
* FAQ
### Layers on Top of Storm
#### Trident
Trident是Storm可供选择的接口。它提供恰好执行一次(exactly-once)，事物性持久存储和流处理选项命令集。
* Trident教程 -- 基本概念和演示
* Trident API综述 -- 转换操作和数据编排
* Trident状态 -- 仅执行一次和快速地，持久集合
* Trident spouts -- 事物数据和非事物数据引入
* Trident RAS API -- 在Trident中使用Resource Aware Scheduler
#### SQL
Strom SQL集合允许用户通过Storm在流式数据上进行SQL查询。
**注意：**Storm SQL是实验性特性，因此Storm SQL 内部及其所支持的特性可能随时调整。但是小的调整不会影响到用户体验。当引入调整破坏了用户体验时我们会通知用户。
* Storm SQL概述
* Storm SQL样例
* Storm SQL参考
* Storm SQL机制

#### Flux
Flux Data Driven Topology Builder

#### 安装和部署
* 安装Storm集群
* 本地模式
* 故障排错
* 在生产集群上运行topologies
* 使用Maven创建Storm
* 安装安全的集群
* 在大集群上使用zookeeper
* 监控守护进程
* Windows用户指南
#### 中级
* 序列化
* 通用模式
* Clojure DSL
* 在非JVM预言上使用Storm
* 分布式RPC
* 事务性topologies
* Hooks
* (Metrics)度量
* 状态检查点
* 窗口
* 加入流
* Blobstore(Distcahce)

#### 调试
* 动态日志等级设置
* 查找Worker日志
* Worker性能分析
* 事件日志
#### 集成外部系统和其他库
* 集成Kafka，新Kafka消费者集成
* 集成HBase
* 集成HDFS
* 集成Hive
* 集成Solr
* 集成Cassandra
* 集成JDBC
* 集成JMS
* 集成Redis
* 集成Event Hubs
* 集成Elasticsearch
* 集成MQTT
* 集成Mongodb
* 集成OpenTSDB
* 集成Kinesis
* 集成Druid
* 集成Kestrel
#### 容器, 资源管理系统集成
* 集成YARN-通过Slider集成YARN
* 集成Mesos
* 集成Docker
* 集成Kubernetes
#### 高级
Defining a non-JVM language DSL for Storm
Multilang protocol (how to provide support for another language)
Implementation docs