# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-03-21

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): 1.5

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): master(替换1.5分支的最新commit)

## Test module

- ~~async~~
- attachment 白泽
- chain[新增] 白泽
- config-api[新增] 白泽
- configcenter
    - ~~apollo~~
    - ~~nacos~~
    - zookeeper 白泽
- context 白泽
- ~~direct~~ 
- docker zhangxun done
- filter zhangxun 

    - ~~custom_filter~~
    - ~~tpslimit~~
    - sentinel  done

- general tiecheng

    - ~~dubbo~~
    - ~~grpc~~
    - jsonrpc
    - rest 

- ~~generic~~ 
- group tiecheng
- ~~hello world~~

- ~~metric~~

- multi-registry zhangxun

- multi-zone zhangxun

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

- seata zhangxun

- shop zhangxun done

- tracing fengzhenyu

# 非共性问题

