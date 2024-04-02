---
sidebar_position: 1
---

# 教程介绍

让我们在 **5 分钟内** 为 `Bukkit` 服务器配置并使用 InkOS。

### 你需要什么？
- [Spigot](https://www.spigotmc.org/) 1.12.2 及以上，推荐使用 [Paper](https://papermc.io/software/paper)
- [InkOS](https://github.com/) bukkit 版本

## 安装插件

1. 将 InkOS 插件放入 `plugins` 文件夹
2. 重启服务器

## 为自己设置一个变量
在服务器中输入以下命令：
```
/inkos set dev.hello world
```

这段命令将会为您自己设置变量 `dev.hello` 为 `world`。

## 获取刚刚设置的变量
在服务器中输入以下命令：
```
/inkos get dev.hello
```

这段命令将会获取到您刚刚设置的变量 `dev.hello` 的值。

## 使用 PlaceHolderAPI 获取变量（可选）
在服务器中输入以下命令：
```
/papi parse me %inkos_dev.hello%
```

这段命令将会通过 `PlaceHodlerApi` 获取到您刚刚设置的变量 `dev.hello` 的值，你也可以在其他支持 `PlaceHolderAPI` 的地方使用这个变量。


### 为什么不开源？
简单来说就是，用了点不该用的代码（逃

不过插件没有混淆，你可以完全通过反编译来查看源码，我们绝不会阻止你这么做。
