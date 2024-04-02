---
sidebar_position: 1
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# 基础 API 使用

## 添加 Ankh Plugin Repository
<Tabs groupId="build-system-type">
<TabItem value="gradle-kts" label="Gradle kts" default>
添加 Maven 仓库到 build.gradle.kts 文件：
```kotlin title="build.gradle.kts"
repositories {
    maven("https://packages.inksnow.org/maven/p/ankh-plugin/maven")
}
```
</TabItem>
<TabItem value="gradle" label="Gradle groovy">
添加 Maven 仓库到 build.gradle.kts 文件：
```groovy title="build.gradle"
repositories {
    maven { url 'https://packages.inksnow.org/maven/p/ankh-plugin/maven' }
}
```
</TabItem>
<TabItem value="maven" label="Maven">
添加 Maven 仓库到 pom.xml 文件：
```xml title="pom.xml"
<repositories>
    <repository>
        <id>ankh-plugin</id>
        <url>https://packages.inksnow.org/maven/p/ankh-plugin/maven</url>
    </repository>
</repositories>
```
</TabItem>
</Tabs>

## 添加依赖
<Tabs groupId="build-system-type">
<TabItem value="gradle-kts" label="Gradle kts" default>
添加依赖到 build.gradle.kts 文件：
```kotlin title="build.gradle.kts"
dependencies {
    compileOnly("bot.inker.inkos:bukkit-api:1.0.13")
}
```
</TabItem>
<TabItem value="gradle" label="Gradle groovy">
添加依赖到 build.gradle.kts 文件：
```groovy title="build.gradle"
dependencies {
    compileOnly 'bot.inker.inkos:bukkit-api:1.0.13'
}
```
</TabItem>
<TabItem value="maven" label="Maven">
添加依赖到 pom.xml 文件：
```xml title="pom.xml"
<dependency>
    <groupId>bot.inker.inkos</groupId>
    <artifactId>bukkit-api</artifactId>
    <version>1.0.13</version>
    <scope>provided</scope>
</dependency>
```
</TabItem>
</Tabs>

## 使用 API

InkOS.get* 接受的参数为 `Player`、 `key` 及 `defaultValue`，其中 `Player` 为玩家对象，`key` 为变量名称，`defaultValue` 为默认值。`defaultValue` 可以被省略。

InkOS.require* 接受的参数为 `Player` 及 `key`，其中 `Player` 为玩家对象，`key` 为变量名称。

当变量不存在时，`InkOS.get*` 会返回 `defaultValue`，如未指定 `defaultValue` 则返回 `null`。而 `InkOS.require*` 会抛出 `IllegalArgumentException`。

InkOS.set* 接受的参数为 `Player`、 `key` 及 `value`，其中 `Player` 为玩家对象，`key` 为变量名称，`value` 为变量值。

```java
import bot.inker.inkos.InkOS;

InkOS.setBytes(player, "dev.testbytes", new byte[]{ 1, 2, 3});
InkOS.getBytes(player, "dev.testbytes"); // [1, 2, 3]
InkOS.getBytes(player, "dev.testbytes1"); // null
InkOS.getBytes(player, "dev.testbytes", new byte[2, 3,4]); // [1, 2, 3]
InkOS.getBytes(player, "dev.testbytes1", new byte[2, 3,4]); // [2, 3, 4]
InkOS.requireBytes(player, "dev.testbytes"); // [1, 2, 3]
InkOS.requireBytes(player, "dev.testbytes1"); // throw IllegalArgumentException

InkOS.setString(player, "dev.teststring", "world");
InkOS.getString(player, "dev.teststring"); // "world"

InkOS.setInt(player, "dev.testint", 123);
InkOS.getInt(player, "dev.testint"); // 123

InkOS.setLong(player, "dev.testlong", 1234567890L);
InkOS.getLong(player, "dev.testlong"); // 1234567890

InkOS.setDouble(player, "dev.testdouble", 123.456);
InkOS.getDouble(player, "dev.testdouble"); // 123.456

InkOS.setBoolean(player, "dev.testboolean", true);
InkOS.getBoolean(player, "dev.testboolean"); // true

InkOS.setBigInteger(player, "dev.testbiginteger", new BigInteger("123456789012345678901234567890"));
InkOS.getBigInteger(player, "dev.testbiginteger"); // 123456789012345678901234567890

InkOS.setBigDecimal(player, "dev.testbigdecimal", new BigDecimal("123456789012345678901234567890.123456789"));
InkOS.getBigDecimal(player, "dev.testbigdecimal"); // 123456789012345678901234567890.123456789
```
