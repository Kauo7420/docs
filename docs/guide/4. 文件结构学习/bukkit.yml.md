---
title: bukkit.yml
icon: bxs:file
createTime: 2026/02/05 00:28:52
permalink: /guide/wen-jian-jie-gou-xue-xi/bukkit-yml/
foo: foo
tags:
    - 文件
---
::: info

本文章所述内容仅适用于`Bukkit`/`Spigot`及其分支服务器。
:::

## 概述
`Bukkit.yml` 是一个用于配置 ==CraftBukkit=={.warning} 或其衍生服务器软件（如 ==Spigot== 或 ==Paper==）的高级设置的文件。这个文件包含了服务器的各种配置选项，允许管理员微调服务器的各个方面，从性能到游戏玩法。

## 源文件内容
由于`Bukkit.yml`的内容可能会根据服务器软件的具体版本有所不同，以下是一些常见的顶级配置选项及其默认值和描述：

```yaml
# General CraftBukkit server options.
is-the-end-enabled: true
show-overloaded-messages: true
custom-permissions-file: permissions.yml
plugin-update-folder: update
max-packets-per_second: 100
use-exact-login-location: false
world-directory: ""
enable-timings: false
connection-throttle: 0
return-plugins-list: true
warn-deprecated-events: default
server-shutdown-message: "Server closed"
prevent-incompatible-plugins: none
```



## 配置项详解
#### **is-the-end-enabled**
+ **类型**: 布尔值
+ **作用**: 控制是否开启“末地”维度。
+ **如何配置**: 设为 `true` 或 `false`。
+ **默认值**: `true`

#### show-overloaded-messages
+ **类型**: 布尔值
+ **作用**: 控制服务器是否显示过载警告信息。
+ **如何配置**: 设为 `true` 或 `false`。
+ **默认值**: `true`

#### custom-permissions-file
+ **类型**: 字符串
+ **作用**: 指定自定义权限文件的名称。
+ **如何配置**: 修改文件名字符串。
+ **默认值**: `permissions.yml`

#### plugin-update-folder
+ **类型**: 字符串
+ **作用**: 指定更新插件时存放更新文件的文件夹名称。
+ **如何配置**: 修改文件夹名字符串。
+ **默认值**: `update`
+ **注意事项**: 文件夹必须位于插件文件夹内。

#### max-packets-per_second
+ **类型**: 整数
+ **作用**: 最大化游戏内ping列表使用的每秒数据包数量。
+ **如何配置**: 修改整数值。
+ **默认值**: `100`
+ **当前状态**: 已禁用。

#### use-exact-login-location
+ **类型**: 布尔值
+ **作用**: 控制玩家登录时是否直接返回到他们注销的确切位置。
+ **如何配置**: 设为 `true` 或 `false`。
+ **默认值**: `false`

#### world-directory
+ **类型**: 字符串
+ **作用**: 指定存储所有世界目录的文件夹名称。
+ **如何配置**: 修改文件夹名字符串。
+ **默认值**: 当前工作目录。

#### enable-timings
+ **类型**: 布尔值
+ **作用**: 启用命令`/timings`，用于测量插件事件的耗时。
+ **如何配置**: 设为 `true` 或 `false`。
+ **默认值**: `false`

#### connection-throttle
+ **类型**: 长整型
+ **作用**: 客户端再次连接前的延迟，单位为毫秒。
+ **如何配置**: 修改长整型数值。
+ **默认值**: `0`
+ **注意事项**: 0 表示禁用连接节流。

#### return-plugins-list
+ **类型**: 布尔值
+ **作用**: 控制远程查询时是否返回插件列表。
+ **如何配置**: 设为 `true` 或 `false`。
+ **默认值**: `true`

#### warn-deprecated-events
+ **类型**: 字符串
+ **作用**: 控制是否警告已弃用的事件注册。
+ **如何配置**: 设为 `true`、`false` 或 `default`。
+ **默认值**: `default`

#### server-shutdown-message
+ **类型**: 字符串
+ **作用**: 服务器关闭时向客户端显示的消息。
+ **如何配置**: 修改字符串。
+ **默认值**: `"Server closed"`

#### prevent-incompatible-plugins
+ **类型**: 字符串
+ **作用**: 阻止不兼容API的插件加载。
+ **如何配置**: 修改字符串。
+ **默认值**: `none`

## 数据库配置
`Bukkit.yml` 还包含数据库配置部分，允许你指定服务器将如何与数据库进行通信，无论是 SQLite 还是 MySQL 等。

## 世界生成器
`Bukkit.yml` 也允许你定义默认加载的世界生成器。

---

::: tip

在进行任何配置更改时，总是备份原始文件以防万一需要恢复到默认设置。
:::

感谢大家的耐心观看啦~，我是卡沃，咱们下个教程再见qwq！

