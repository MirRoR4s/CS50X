# SQL

## 前言

本周以 `sqlite` 为基础讲述 SQL（结构化查询语言）的基本用法，包括基本的增删改查语句等。

## sqlite 简介

sqlite 是一种关系型数据库。在关系型数据库中，数据被存储在由行和列组成的表格中，一个数据库可能会含有多个表格。

sqlite 文件由 `.db` 结尾，可在命令行键入 `sqlite3 a.db` 打开一个名为 a.db 的 sqlite 文件，并在打开 sqlite 之后键入 `.schema` 查看创建表时执行的 SQL 语句，这能够帮助我们理解数据库中表的结构。

打开 sqlite 之后可键入 `.mode csv` 进入 csv 模式，此时就可以导入外部的 CSV 文件并根据文件的内容自动创建数据库，具体语法是 `.import {csv文件名} {数据库名} `。

---

## sqlite crud

假设有一个名为 favorites 的表，其结构如下：

```sql
CREATE TABLE IF NOT EXISTS "favorites"(
"Timestamp" TEXT, "language" TEXT, "problem" TEXT);
```

favorites 表包含三列，分别是 Timestamp 和 language 以及 problem。

### 插入数据

- 向 favorites 表插入一行数据（指明列名以及对应的数据）：

```sql
INSERT INTO favorites (Timestamp, language, problem) VALUES ("10/30/2023 13:38:19", "Python", "Hello, World");
```

### 查询数据

- 查询 favorites 表中所有列的数据：

```sql
SELECT * FROM favorites;
```

- 查询 favorites 表 language 列的数据：

```sql
SELECT language FROM favorites;
```

### 更新数据

- 将 favorites 表的 language 列修改为 Java：

```sql
UPDATE favorites SET language = "Java";
```

### 删除数据

- 删除 favorites 表的所有数据：

```sql
DELETE FROM favorites;
```

### 