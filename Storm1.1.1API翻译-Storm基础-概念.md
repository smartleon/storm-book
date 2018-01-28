---
title: Storm1.1.1API翻译-Storm基础-概念 
tags: Storm概念
grammar_cjkRuby: true
---
本页面列出了Storm的主要概念和其他相关的资源链接。讨论的概念如下：
1.Topologies
2.Streams
3.Spouts
4.Bolts
5.Stream groupings(Stream分组策略)
6.Reliability (可靠性)
7.Tasks
8.Workers
### Topologies
实时应用程序的逻辑被打包到Storm topology中。一个Storm topology类似于MapReduce的job。其中一个关键的不同点是MapReduce job最终会停止，但topology会永远运行下去(除非手动杀掉它)。一个topology就是一个spout和blot通过Stream分组连接的示意图。相关概念描述如下。
#### Resources:
* [TopologyBuilder](http://storm.apache.org/releases/1.1.1/javadocs/org/apache/storm/topology/TopologyBuilder.html): 使用该java类创建
* [在生产集群上运行Topologies](xxxx)
* [本地模式](xxxxx): 本篇主要介绍如何在开发程序及在本地模式下测试。
### Streams
The stream is the core abstraction in Storm. A stream is an unbounded sequence of tuples that is processed and created in parallel in a distributed fashion. Streams are defined with a schema that names the fields in the stream's tuples. By default, tuples can contain integers, longs, shorts, bytes, strings, doubles, floats, booleans, and byte arrays. You can also define your own serializers so that custom types can be used natively within tuples.
stream是Storm的核心抽象。stream是无限的tuple序列，在平行的分布式系统中被执行和创建。Stream是stream的tuple的命名模式。默认情况下，tuples可以包含integers, longs, shorts, bytes, strings, doubles, floats, booleans以及byte arrays。你也可以自己定义序列化器以便自定义的类型可以被自然的在tuple中使用。

Every stream is given an id when declared. Since single-stream spouts and bolts are so common, OutputFieldsDeclarer has convenience methods for declaring a single stream without specifying an id. In this case, the stream is given the default id of "default".
在声明stream时，每一个stream都会被设置一个ID。单独stream、spouts和bolts都是通用的，OutputFieldsDeclarer有方便的方法在不说明id的情况下去声明一个单独的stream。因此，这样的stream的id被设置为"default"。

#### Resources:
* [Tuple](xxxxx): streams由tuple组成。
* [OutputFieldsDeclarer](xxxxx): 被用来声明stream及其模式
* [Serialization](xxxx): Storm动态类型和声明自定义序列化信息。
### Spouts
A spout is a source of streams in a topology. Generally spouts will read tuples from an external source and emit them into the topology (e.g. a Kestrel queue or the Twitter API). Spouts can either be reliable or unreliable. A reliable spout is capable of replaying a tuple if it failed to be processed by Storm, whereas an unreliable spout forgets about the tuple as soon as it is emitted.
spout是topology中streams
Spouts can emit more than one stream. To do so, declare multiple streams using the declareStream method of OutputFieldsDeclarer and specify the stream to emit to when using the emit method on SpoutOutputCollector.

The main method on spouts is nextTuple. nextTuple either emits a new tuple into the topology or simply returns if there are no new tuples to emit. It is imperative that nextTuple does not block for any spout implementation, because Storm calls all the spout methods on the same thread.

The other main methods on spouts are ack and fail. These are called when Storm detects that a tuple emitted from the spout either successfully completed through the topology or failed to be completed. ack and fail are only called for reliable spouts. See the Javadoc for more information.

Resources:

IRichSpout: this is the interface that spouts must implement.
Guaranteeing message processing
这是真不错