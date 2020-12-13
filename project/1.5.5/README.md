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
* general: watermelo - done
    * dubbo - done (integration)
    * jsonrpc - done (integration)
    * grpc - done (integration)
    * rest - done (integration)
* generic: watermelo - done (integration)
* helloworld: haohongfan - done (integration)
* seata: tiecheng - done (integration)
* registry haohongfan
	* etcd: done --- ~~grpc v1.27.0 与 etcd@v3.3.25 不兼容~~
	* nacos: done
	* kubernetes: done
* registry/servicediscovery haohongfan
	* consul: done ~~没修改成适应makefile的版本~~
	* file:  done ~~Failed to check the status of the service org.apache.dubbo.UserProvider. No provider available for the service to the consumer use dubbo version 1.3.0~~
	* etcd: done ~~同样版本问题~~
	* nacos: done
	* zk: done
* multi-registry: haohongfan - done
* service discovery: zouyx
    * zk - done (integration)
    * nacos - done
* metric: zouyx - done (integration)
* router: zouyx - 模块代码没问题，但依然存在启动需要停 5s 等router 代码准备好的问题。
* shop: zhangxun - done (integration)
* tracing : zouyx - done

# 非共性问题
## 与 2.7.7 路径不兼容
解决人：fangyincheng
例子：
解决结果：
https://github.com/apache/dubbo-go/pull/914

## etcd: grpc v1.27.0 与 etcd@v3.3.25 不兼容 -- **done**
解决人：lizhixin
例子：registry/etcd 与 registry/servicediscovery/etcd
解决结果：
https://github.com/apache/dubbo-go-samples/pull/21

## 没修改成适应makefile的版本 -- **done**
解决人：zhangxun
例子：registry/servicediscovery/consul
解决结果：
https://github.com/apache/dubbo-go-samples/pull/22

## 不能找到 provider -- **done**
Failed to check the status of the service org.apache.dubbo.UserProvider. No provider available for the service to the consumer use dubbo version 1.3.0 
解决人：tiecheng
例子：registry/servicediscovery/file
解决结果：done
https://github.com/apache/dubbo-go-samples/pull/23
https://github.com/apache/dubbo-go/pull/932


## 存在启动需要停 5s 等router 代码准备好才能使用 - done
期望:需要启动完成马上能启动
https://github.com/apache/dubbo-go/pull/758
看看结合这个是否能解决
解决人：zouyx
例子：router
解决结果：done
https://github.com/apache/dubbo-go/pull/927

## 远程 meta data 获取数据空指针
解决人：jiangchao
例子：registry/servicediscovery/zookeeper ，其中需要改成远程配置中心
解决结果：

# 共性问题: **不是问题**
## mac上sentinel-golang
解决人:已通知 sentinel-go 进行排查
提示: Failed to retrieve current CPU usage: not implemented yet
解决结果：


## 循环引用: 不是循环依赖问题.  envoyproxy/go-control-plane 那个包需要升一个小版本，但是升的小版本那个单元测试需要用 1.14 才能跑

需要升级github action go版本

解决人：watermelo
dubbo-go-samples `go mod tidy` 提示下面问题:

```
$ go mod tidy
go: downloading github.com/envoyproxy/go-control-plane v0.9.1-0.20191026205805-5f8ba28d4473
go: finding module for package github.com/envoyproxy/go-control-plane/pkg/util
go: downloading github.com/envoyproxy/go-control-plane v0.9.8
github.com/apache/dubbo-go-samples/registry/servicediscovery/consul/go-client/app imports
	github.com/apache/dubbo-go/metadata/report/consul tested by
	github.com/apache/dubbo-go/metadata/report/consul.test imports
	github.com/apache/dubbo-go/remoting/consul imports
	github.com/hashicorp/consul/agent imports
	github.com/hashicorp/consul/agent/xds imports
	github.com/envoyproxy/go-control-plane/pkg/util: module github.com/envoyproxy/go-control-plane@latest found (v0.9.8), but does not contain package github.com/envoyproxy/go-control-plane/pkg/util
```
解决结果：
