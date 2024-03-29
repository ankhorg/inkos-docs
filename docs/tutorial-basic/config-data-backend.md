---
sidebar_position: 1
---

# 配置数据存储后端

InkOS 支持多种数据存储后端，你可以在 `config.yml` 中配置你的数据存储后端。

配置示例：
```yaml title="plugins/InkOS/config.yml"
dataBackends:
  example-posgres:
    type: postgres
    host: localhost:5432
    database: inkos
    username: inkos
    password: inkos
  example-mysql:
    type: mysql
    host: localhost:3306
    database: inkos
    username: inkos
    password: inkos
  example-inkdb:
    type: inkdb
    path: ./db/inkdb
  example-leveldb:
    type: leveldb
    path: ./db/leveldb
```

在 `dataBackends` 中配置你的数据存储后端，你可以配置多个数据存储后端，每个数据存储后端都需要一个唯一的名称。

在示例中，我们配置了四个数据存储后端，其名称 `example-posgres`、`example-mysql`、`example-inkdb` 和 `example-leveldb`。

在每一个数据存储后端中，你需要配置 `type` 字段，用于指定数据存储后端的类型，你还需要配置相应的数据存储后端的配置。

## 支持的数据存储后端
### [PostgreSQL](https://www.postgresql.org/)

PostgreSQL 需要四个配置项：

- `host` 数据库地址，格式为 `host:port`
- `database` 数据库名称
- `username` 数据库用户名
- `password` 数据库密码

### [MySQL](https://www.mysql.com/)

MySQL 需要四个配置项：

- `host` 数据库地址，格式为 `host:port`
- `database` 数据库名称
- `username` 数据库用户名
- `password` 数据库密码

### InkDB
InkDB 是 InkOS 专为 `Minecraft` 设计的存储后端，它是一个基于文件的多进程共享数据库。

您可以在一个系统上运行多个服务器，这些服务器可以共享一个数据库，只需要您将他们的 `path` 设为同一个。

InkDB 需要一个配置项：

- `path` 数据库文件存储路径

### [LevelDB](https://github.com/google/leveldb)

LevelDB 是一个快速的键值存储库，其速度快于大多数数据库，但是其不支持多进程共享。

LevelDB 需要一个配置项：

- `path` 数据库文件存储路径

## 数据存储后端的选择

- 如果你的服务器是单个独立的服务器，推荐使用 `LevelDB`。
- 如果你的服务器是多个服务器，但运行在同一个系统上，推荐使用 `InkDB`。
- 如果你的服务器连接多个系统，或使用其他隔离技术（如 `docker`），推荐使用 `PostgreSQL` 或 `MySQL`。

