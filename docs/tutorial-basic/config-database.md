---
sidebar_position: 2
---

# 配置数据库

```yaml title="plugins/InkOS/config.yml"
databases:
  dev:
    source: example-postgres
    tableName: inkos_player_pvc_dev
  dev1:
    source: example-mysql
    tableName: inkos_player_pvc_dev
  dev2:
    source: example-inkdb
    prefix: test
  dev3:
    source: example-leveldb
    prefix: test
```

在 `databases` 中配置你的数据库，你可以配置多个数据库，每个数据库都需要一个唯一的名称。

在示例中，我们配置了四个数据库，其名称 `dev0`、`dev1`、`dev2` 和 `dev3`。

在每一个数据库中，你需要配置 `source` 字段，用于指定数据存储后端的名称，你还需要配置相应的数据库的配置。

## 数据后端需要的其他配置

### PostgreSQL

PostgreSQL 需要一个配置项：

- `tableName` 数据库表名

### MySQL

MySQL 需要一个配置项：

- `tableName` 数据库表名

### InkDB

InkDB 需要一个配置项：

- `prefix` 存储前缀

### LevelDB

LevelDB 需要一个配置项：

- `prefix` 存储前缀

## 数据库使用

在使用时，InkOS 会根据变量名，自动选择对应的数据库进行操作。

例如，当你使用 `dev.hello` 时，InkOS 会根据 `dev` 自动选择 `dev` 数据库进行操作。
