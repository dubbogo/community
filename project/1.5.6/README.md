# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-02-10

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): 1.5

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): 1.5.6

## Test module

- ~~async~~
- attachment 白泽
- configcenter
    - ~~apollo~~
    - ~~nacos~~
    - zookeeper 白泽

- ~~direct~~

- filter

    - ~~custom_filter~~
    - ~~tpslimit~~
    - sentinel 白泽

- general

    - ~~dubbo~~
    - ~~grpc~~
    - jsonrpc 白泽
    - rest 白泽

- ~~generic~~

- ~~hello world~~

- ~~metric~~

- multi-registry tiecheng - done

- multi-zone tiecheng - done

- router

    - ~~condition~~
    - tag tiecheng

- registry zhangxun

    - etcd - done
    - kubernetes
    - nacos - done
    - servicediscovery zhangxun
        - ~~zookeeper~~- 启动异常
        - consul - done
        - etcd - provider 和 consumer 配置了不同的application.name 后 consumer 找不到服务提供者
        - file - 启动异常
        - nacos - done

- seata tiecheng - done

- shop tiecheng - done

- tracing tiecheng - done

# 非共性问题

