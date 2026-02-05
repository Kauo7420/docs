---
title: server.properties
icon: bxs:file
createTime: 2026/02/05 00:28:41
permalink: /guide/wen-jian-jie-gou-xue-xi/server-properties/
foo: foo
tags:
    - 文件
---
::: important
🚧施工中……🚧
:::
## 文件简介
`server.properties` 是Minecraft服务器的==核心配置文件==，用于存储和管理服务器的各种设置，从基本的网络参数到游戏规则和安全选项。编辑这个文件可以让你定制服务器的各个方面，以满足特定的游戏体验需求。

合理的配置该文件，可以使你的服务器达到一个良好的运维效果。

## 原配置文件内容
以下是Minecraft ==Java版1.21==中`server.properties`文件的部分默认配置示例：

### **Java版**
```properties
#Minecraft server properties
#（时间戳）
accepts-transfers=false
allow-flight=false
allow-nether=true
broadcast-console-to-ops=true
broadcast-rcon-to-ops=true
bug-report-link=
difficulty=easy
enable-command-block=false
enable-jmx-monitoring=false
enable-query=false
enable-rcon=false
enable-status=true
enforce-secure-profile=true
enforce-whitelist=false
entity-broadcast-range-percentage=100
force-gamemode=false
function-permission-level=2
gamemode=survival
generate-structures=true
generator-settings={}
hardcore=false
hide-online-players=false
initial-disabled-packs=
initial-enabled-packs=vanilla
level-name=world
level-seed=
level-type=minecraft\:normal
log-ips=true
max-chained-neighbor-updates=1000000
max-players=20
max-tick-time=60000
max-world-size=29999984
motd=A Minecraft Server
network-compression-threshold=256
online-mode=true
op-permission-level=4
player-idle-timeout=0
prevent-proxy-connections=false
pvp=true
query.port=25565
rate-limit=0
rcon.password=
rcon.port=25575
region-file-compression=deflate
require-resource-pack=false
resource-pack=
resource-pack-id=
resource-pack-prompt=
resource-pack-sha1=
server-ip=
server-port=25565
simulation-distance=10
spawn-animals=true
spawn-monsters=true
spawn-npcs=true
spawn-protection=16
sync-chunk-writes=true
text-filtering-config=
use-native-transport=true
view-distance=10
white-list=false
```

### 解释配置选项
| **配置项** | **类型** | **描述** | **默认值** |
| --- | --- | --- | --- |
| accepts-transfers | 布尔值 | 控制是否接受从其他服务器转移来的玩家。 | false |
| allow-flight | 布尔值 | 允许玩家在生存模式下飞行。 | false |
| allow-nether | 布尔值 | 允许玩家进入下界。 | true |
| broadcast-console-to-ops | 布尔值 | 是否广播控制台消息给操作员。 | true |
| broadcast-rcon-to-ops | 布尔值 | 是否广播RCON消息给操作员。 | true |
| difficulty | 字符串 | 设置游戏难度。 | easy |
| enable-command-block | 布尔值 | 是否启用命令方块。 | false |
| enable-jmx-monitoring | 布尔值 | 启用JMX监控。 | false |
| enable-query | 布尔值 | 是否启用查询接口。 | false |
| enable-rcon | 布尔值 | 是否启用远程控制。 | false |
| enable-status | 布尔值 | 是否在服务器列表中显示为在线。 | true |
| enforce-secure-profile | 布尔值 | 是否强制使用安全的Mojang签名。 | true |
| enforce-whitelist | 布尔值 | 是否强制执行白名单。 | false |
| entity-broadcast-range-percentage | 整数 | 实体广播范围的百分比。 | 100 |
| force-gamemode | 布尔值 | 是否强制玩家的游戏模式。 | false |
| function-permission-level | 整数 | 函数的默认权限等级。 | 2 |
| gamemode | 字符串 | 默认游戏模式。 | survival |
| generate-structures | 布尔值 | 是否生成结构。 | true |
| generator-settings | 字符串 | 世界生成设置。 | (空) |
| hardcore | 布尔值 | 是否启用硬核模式。 | false |
| hide-online-players | 布尔值 | 是否隐藏在线玩家列表。 | false |
| initial-disabled-packs | 字符串 | 初始禁用的数据包。 | (空) |
| initial-enabled-packs | 字符串 | 初始启用的数据包。 | vanilla |
| level-name | 字符串 | 世界的名称。 | world |
| level-seed | 字符串 | 世界的种子。 | (空) |
| level-type | 字符串 | 世界类型。 | minecraft:normal |
| log-ips | 布尔值 | 是否记录IP地址。 | true |
| max-chained-neighbor-updates | 整数 | 最大链接邻居更新次数。 | 1000000 |
| max-players | 整数 | 最大玩家数量。 | 20 |
| max-tick-time | 整数 | 最大tick时间。 | 60000 |
| max-world-size | 整数 | 最大世界尺寸。 | 29999984 |
| motd | 字符串 | 服务器Motd信息。 | A Minecraft Server |
| network-compression-threshold | 整数 | 网络压缩阈值。 | 256 |
| online-mode | 布尔值 | 是否需要玩家在线验证。 | true |
| op-permission-level | 整数 | 操作员的权限等级。 | 4 |
| player-idle-timeout | 整数 | 玩家空闲超时时间。 | 0 |
| prevent-proxy-connections | 布尔值 | 是否阻止代理连接。 | false |
| pvp | 布尔值 | 是否允许PVP。 | true |
| query.port | 整数 | 查询端口。 | 25565 |
| rate-limit | 整数 | 速率限制。 | 0 |
| rcon.password | 字符串 | RCON密码。 | (空) |
| rcon.port | 整数 | RCON端口。 | 25575 |
| region-file-compression | 字符串 | 区域文件压缩算法。 | deflate |
| require-resource-pack | 布尔值 | 是否需要资源包。 | false |
| resource-pack | 字符串 | 资源包URL。 | (空) |
| resource-pack-id | 字符串 | 资源包标识。 | (空) |
| resource-pack-prompt | 字符串 | 资源包提示。 | (空) |
| resource-pack-sha1 | 字符串 | 资源包SHA1校验和。 | (空) |
| server-ip | 字符串 | 服务器IP地址。 | (空) |
| server-port | 整数 | 服务器端口。 | 25565 |
| simulation-distance | 整数 | 模拟距离。 | 10 |
| spawn-animals | 布尔值 | 是否生成动物。 | true |
| spawn-monsters | 布尔值 | 是否生成怪物。 | true |
| spawn-npcs | 布尔值 | 是否生成NPC。 | true |
| spawn-protection | 整数 | 生成保护半径。 | 16 |
| sync-chunk-writes | 布尔值 | 是否同步区块写入。 | true |
| text-filtering-config | 字符串 | 文本过滤配置。 | (空) |
| use-native-transport | 布尔值 | 是否使用原生传输。 | true |
| view-distance | 整数 | 视野距离。 | 10 |
| white-list | 布尔值 | 是否启用白名单。 | false |


::: tip 你知道吗

Java版24w33a加入了新选项：`pause-when-empty-seconds`（默认为`60`），它可以控制服务器在无人在线状态多少秒之后暂停服务器。
:::

# 手动配置
## 示例实操
+ 打开`server.properties`文件，通常位于服务器根目录。
+ 查找想要修改的配置项。
+ 删除配置项前面的`#`注释符号。
+ 修改配置项后面的值。
+ 保存并关闭文件。
+ 重启服务器以应用更改。

## 注意事项
+ 修改配置后，记得重启服务器以使更改生效。
+ 不要修改配置项的名称，只修改等号后的值。
+ 保存更改前，确保所有更改都是正确的，以避免服务器启动失败。
+ 如果添加了新的配置项，服务器会自动在下次启动时补全缺失的配置，并使用默认值。

通过编辑`server.properties`，你可以定制服务器的多个方面，以适应不同的游戏场景和需求。

感谢大家的耐心观看啦~，我是卡沃，咱们下个教程再见qwq！

