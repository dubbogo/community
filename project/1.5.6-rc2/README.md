# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-03-21

## Test branch

[dubbo-go](https://github.com/apache/dubbo-go/): 1.5

[dubbo-go-sample](https://github.com/apache/dubbo-go-samples/): master(替换1.5分支的最新commit)

## Test module

- ~~async~~
- attachment 白泽 done
- chain[新增] 白泽 done
- config-api[新增] 白泽 done
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
    - jsonrpc done
    - rest done

- ~~generic~~ 
- group tiecheng done
- ~~hello world~~

- ~~metric~~

- multi-registry zhangxun done

- multi-zone zhangxun done

- router

    - ~~condition~~
    - tag 这个应该是有问题的，目前找志信，白泽都看过。和部长确认没有真实使用，所以直接到 3.0 去包含或者后面实际场景完善了再打补丁

- registry fengzhenyu

    - etcd done
    - kubernetes done
    - nacos done (不兼容nacos2.0)
    - servicediscovery
        - ~~zookeeper~~
        - consul done
        - etcd done
        - file done
        - nacos done(不兼容nacos2.0)

- seata zhangxun done

- shop zhangxun done

- tracing fengzhenyu done

# 非共性问题
    jsonrpc 启动warn can not connect to a server, 几次重试后连接上去了, 然后又会warn  has already been listened. 不影响调用 但是很奇怪 这块逻辑是不是有毛病?

