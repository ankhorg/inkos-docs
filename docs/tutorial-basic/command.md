---
sidebar_position: 4
---

# 命令及权限节点

## /inkos set

设置一个变量。
```
/inkos set [player] <key> <value>
```

- `player` 玩家名称，如不指定则默认为自己。
- `key` 变量名称。
- `value` 变量值。

权限节点：`inkos.command。admin.set`

## /inkos get

获取一个变量。
```
/inkos get [player] <key>
```

- `player` 玩家名称，如不指定则默认为自己。
- `key` 变量名称。

权限节点：`inkos.command.admin.get`

## /inkos iadd

对一个变量进行整数加法操作。
```
/inkos iadd [player] <key> <value>
```

- `player` 玩家名称，如不指定则默认为自己。
- `key` 变量名称。
- `value` 变量要加上的值，可以为负数。

权限节点：`inkos.command.admin.iadd`

## /inkos dadd

对一个变量进行浮点数加法操作。
```
/inkos dadd [player] <key> <value>
```

- `player` 玩家名称，如不指定则默认为自己。
- `key` 变量名称。
- `value` 变量要加上的值，可以为负数。

权限节点：`inkos.command.admin.dadd`