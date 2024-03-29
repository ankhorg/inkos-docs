---
sidebar_position: 3
---

# 配置玩家锁

```yaml title="plugins/InkOS/config.yml"
lock:
  type: postgres
  host: localhost:5432
  database: inkos
  username: inkos
  password: inkos
  tableName: inkos_player_lock
```

在 `lock` 中配置你的玩家锁，如果你不想使用玩家锁，可以将 `type` 设置为 `none`。

## 支持的玩家锁存储后端

### [PostgreSQL](https://www.postgresql.org/)

PostgreSQL 需要五个配置项：

- `host` 数据库地址，格式为 `host:port`
- `database` 数据库名称
- `username` 数据库用户名
- `password` 数据库密码
- `tableName` 数据库表名

### [MySQL](https://www.mysql.com/)

MySQL 需要五个配置项：

- `host` 数据库地址，格式为 `host:port`
- `database` 数据库名称
- `username` 数据库用户名
- `password` 数据库密码
- `tableName` 数据库表名

## 玩家锁使用

如果你的数据后端为 `PostgreSQL` 或 `MySQL`，你必须使用玩家锁。

如果你的数据后端为 `InkDB` 或 `LevelDB`，你不需要使用玩家锁。

启用玩家锁后，当玩家进入服务器时，InkOS 会自动为玩家创建一个锁，当玩家退出服务器时，InkOS 会自动删除玩家的锁。

当玩家锁启用时，玩家在进入服务器时，InkOS 会检查玩家是否有锁，如果有锁，InkOS 将禁止玩家的所有行为，直到服务器成功为玩家创建一个锁。
