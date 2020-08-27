# 项目管理

## 前期准备

* 制定版本计划，其中包括：
    * 目标
    * 里程碑
    * 发布日期
    * 任务及负责人
    * 风险
    * 问题
    * reviewer

例子：
![plan](../1.5.2/plan.png)

PS：
1. 其中任务负责人及 reviewer 需要一个个确认时间。
1. 需要在版本开始时间召开启动会。
1. 发布之后，召开总结会，总结经验。

## 发布流程

请参考：[apache-release](https://github.com/wongoo/apache-release-procedure)

### 邮件模版

**发邮件前把 <!--- ---> 中内容删除**

以 v1.5.1 的邮件为例。

```
Hello Dubbo/Dubbogo Community,

  This is a call for vote to release Apache dubbo-go version v1.5.1.

  The release candidates:
https://dist.apache.org/repos/dist/dev/dubbo/dubbo-go/v1.5.1/

  Git tag for the release:
https://github.com/apache/dubbo-go/releases/tag/v1.5.1

  Hash for the release tag: 292850223fae4ed73506810efb179ac969fcbf5b  <!--- GitHub 的 commit id --->

  Release Notes: https://github.com/apache/dubbo-go/blob/1.5/CHANGE.md

  The artifacts have been signed with Key :4B87D4B65EEFB515 <!--- 属于你的写到 https://dist.apache.org/repos/dist/dev/dubbo/KEYS 的 sign --->, which can be
found in the keys file: https://dist.apache.org/repos/dist/dev/dubbo/KEYS

  The vote will be open for at least 72 hours or until necessary number of
votes are reached.

 Please vote accordingly:
 [ ] +1 approve
 [ ] +0 no opinion
 [ ] -1 disapprove with the reason

 Thanks,
 The Apache Dubbo-go Team
```

## 打包脚本

稍后提供