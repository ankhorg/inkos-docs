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
```kts
repositories {
    maven("https://packages.inksnow.org/maven/p/ankh-plugin/maven")
}
```
</TabItem>
<TabItem value="gradle" label="Gradle groovy">
添加 Maven 仓库到 build.gradle.kts 文件：
```groovy
repositories {
    maven { url 'https://packages.inksnow.org/maven/p/ankh-plugin/maven' }
}
```
</TabItem>
<TabItem value="maven" label="Maven">
添加 Maven 仓库到 pom.xml 文件：
```xml
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
```kts
dependencies {
    compileOnly("bot.inker.inkos:bukkit-api:1.0.13")
}
```
</TabItem>
<TabItem value="gradle" label="Gradle groovy">
添加依赖到 build.gradle.kts 文件：
```groovy
dependencies {
    compileOnly 'bot.inker.inkos:bukkit-api:1.0.13'
}
```
</TabItem>
<TabItem value="maven" label="Maven">
添加依赖到 pom.xml 文件：
```xml
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
```java
import bot.inker.inkos.InkOS;

InkOS.setBytes(player, "dev.testbytes", new byte[]{ 1, 2, 3});
InkOS.getBytes(player, "dev.testbytes"); // [1, 2, 3]

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
