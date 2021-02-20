# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-02-10

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): 1.5

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): master(替换1.5分支的最新commit)

## Test module

- ~~async~~
- attachment 白泽 done
- configcenter
    - ~~apollo~~
    - ~~nacos~~
    - zookeeper 白泽 done

- ~~direct~~

- filter

    - ~~custom_filter~~
    - ~~tpslimit~~
    - sentinel 白泽 done

- general

    - ~~dubbo~~
    - ~~grpc~~
    - jsonrpc 白泽 done
    - rest 白泽 done

- ~~generic~~

- ~~hello world~~

- ~~metric~~

- multi-registry tiecheng - done

- multi-zone tiecheng - done

- router

    - ~~condition~~
    - tag tiecheng 这个应该是有问题的，目前找志信，白泽都看过。和部长确认没有真实使用，所以直接到 3.0 去包含或者后面实际场景完善了再打补丁

- registry zhangxun

    - etcd - done
    - kubernetes
    - nacos - done
    - servicediscovery zhangxun
        - ~~zookeeper~~ - 启动异常, panic: runtime error: invalid memory address or nil pointer dereference  github.com/apache/dubbo-go/metadata/mapping/dynamic.(*DynamicConfigurationServiceNameMapping).Get(0xc000796050, 0xc0001cd940, 0x1d, 0x0, 0x0, 0x0, 0x0, 0xc00023a650, 0x5, 0x0, ...)
        - consul - done
        - etcd - provider 和 consumer 配置了不同的application.name 后 consumer 找不到服务提供者
        - file - 启动异常, ?[31mERROR?[0m  servicediscovery/service_discovery_registry.go:442      get service instance selector cathe error:Could not find service instance selector withname:random
        - nacos - done

- seata tiecheng - done

- shop tiecheng - done

- tracing tiecheng - done

# 非共性问题

