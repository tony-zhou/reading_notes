# 第1课 了解SQL
## 1.1 数据库基础
### 1.1.1 数据库
* 保存有组织的数据的容器

### 1.1.2 表
* 表 (table)
	* 某种特定类型数据的结构化清单
* 模式 (schema)
	* 关于数据库和表带布局及特性的信息

### 1.1.3 列和数据类型
* 列 (column)
	* 表中的一个字段
* 数据类型 (datatype)
	* 所允许的数据的类型。每个表列都有相应的数据类型，它限制（或允许）该列中存储的数据  

### 1.1.4 行
* 行 (row)
	* 表中的一个纪录 

### 1.1.5 主键
* 主键 (primary key)
	* 一列（或一组列），其值能够唯一标识表中的每一行
* 主键条件
	* 任意两行都不具有相同的主键
	* 每一行都必须具有一个主键（主键列不允许NULL值）
	* 主键列中的值不允许修改或更新
	* 主键值不能重用（如果某行从表中删除，它的主键不能赋给以后的新行）

## 1.2 什么是SQL
* 结构化查询语言 (Structured Query Language)

</br>

# 第2课 检索数据
## 2.1 SELECT语句
* 必须至少给出两条信息 －－ 想选择什么，以及从什么地方选

## 2.2 检索单个列
* `SELECT column FROM table;`

## 2.3 检索多个列
* `SELECT column0, column1, column2 FROM table;`

## 2.4 检索所有列
* `SELECT * FROM table;`

## 2.5 检索不同的值
* `SELECT DISTINCT column FROM table;`
* `DISTINCT关键字必须直接放在列名的前面，作用于所有列，不仅仅是跟在其后的那一列，除非指定的两列完全相同，否则所有的行都会被检索出来`

## 2.6 限制结果
* SQL Server / Access
	* `SELECT TOP integer column FROM table;` 
* DB2
	* `SELECT column FROM table FETCH FIRST integer ROWS ONLY;`
* Oracle
	* `SELECT column FROM table WHERE ROWNUM <= integer;`
* MySQL / MariaDB / PostgreSQL / SQLite
	* `SELECT column FROM table LIMIT integer;`
	* `指定从某行(integer1)开始以及检索的行数(integer0)`
		* `SELECT column FROM table LIMIT integer0 OFFSET integer1;`
		* `SELECT column FROM table LIMIT integer1, integer0;`

## 2.7 使用注释
* 行内注释
	* -- 之后的文本
	* \# 之后的文本
* 多行注释
	* /* .....*/ 之间的任何内容都是注释

</br>

# 第3课 排序检索数据
## 3.1 排序数据
* `SELECT column FROM table ORDER BY column;`
* `ORDER BY子句必须是SELECT语句的最后一条子语句`

## 3.2 按多个列排序
* `SELECT column FROM table ORDER BY column0, column1;`
* `仅当column0相同情况下才对column1排序`

## 3.3 按列位置排序
* `SELECT column FROM table ORDER BY integer0, integer1;`

## 3.4 指定排序方向
* `SELECT column FROM table ORDER BY column0 DESC, column1;`
* `如果想在多个列上进行降序排序，必须对每一列指定DESC关键字`

# 第4课 过滤数据
## 4.1 使用WHERE子句