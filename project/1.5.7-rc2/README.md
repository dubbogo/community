# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-07-03

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): 1.5

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): master(替换1.5分支的最新commit)

## Test module

- ~~async~~
- attachment 
- chain[新增] 
- config-api[新增]
- configcenter
    - ~~apollo~~
    - ~~nacos~~
    - zookeeper
- context
- ~~direct~~ 
- docker
- filter 

    - ~~custom_filter~~
    - ~~tpslimit~~
    - sentinel 

- general

    - ~~dubbo~~
    - ~~grpc~~
    - jsonrpc
    - rest 

- ~~generic~~ 
- group 
- ~~hello world~~

- ~~metric~~

- multi-registry

- multi-zone

- router

    - ~~condition~~
    - tag 这个应该是有问题的，目前找志信，白泽都看过。和部长确认没有真实使用，所以直接到 3.0 去包含或者后面实际场景完善了再打补丁

- registry fengzhenyu

    - etcd
    - kubernetes
    - nacos 
    - servicediscovery
        - ~~zookeeper~~
        - consul
        - etcd
        - file 
        - nacos 

- seata

- shop

- tracing
