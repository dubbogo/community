# Project summary

# Develop Plan


# Testing Plan

Finish date: 2021-07-03

## Test branch

[dubbo-go-pixiu](https://github.com/apache/dubbo-go-pixiu): develop

[pixiu-admin](https://github.com/dubbogo/pixiu-admin): master

## Test module

- admin zhangxun, 
- admin feng zhenyu
  重复增加相同方法映射会在页面上生成两条记录。删除任意一条后，会删除对应proxy api。但是界面上依然会显示有一条记录。

- ratelimit zhangxun, 
  1. uri 中带驼峰路径时, ratelimit 无法正确的匹配到. 梦超已经提PR 修改


