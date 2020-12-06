# Project summary

# Develop Plan


# Testing Plan

Finish date: 2020-12-6

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): develop

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): 1.5.5

## Test module

* aync: zouyx - done (integration)
* configcenter: zouyx - done (integration)
* direct: zouyx - done (integration)
* filter: watermelo - done (integration)
* general: watermelo
    * dubbo - done (integration)
    * jsonrpc - done (integration)
    * grpc - done (integration)
    * rest - done (integration)
* generic: watermelo - done (integration)
* helloworld: haohongfan - done (integration)
* seata: tiecheng - done (integration)
* registry haohongfan
* service discovery: zouyx
    * zk - done (integration)
    * nacos
* multi_registry: haohongfan
* metric: zouyx - done (integration)
* router: zouyx - 模块代码没问题，但依然存在启动需要停 5s 等router 代码准备好的问题。
* shop: zhangxun - done (integration)
* tracing : zouyx - done
