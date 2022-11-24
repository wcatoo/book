## SQLite Basic
SQLite遵循一套独特的语法用于操作数据库。<br>
1. SQLite是不区分大小写的，但是有些命令大小写有不同的语义。
2. SQLite语句结束以";"区分

### 数据存储类型
* NULL 值是一个null
* INTEGER   值是一个带符号的整型
* REAL  值是一个浮点
* TEXT  字符串类型
* BLOB  根据输入存储

### 基本操作
* 创建数据库 sqlite3 [filename]  or .open [filename]
* 附加数据库 如果想同时打开多个数据库 ATTACH DATABASE "[filename]" as "alias name"; <br>
其中"main" "temp" 为系统用于保留主数据库和临时数据库对象的数据库
* 分离数据库 把一个命名数据库从一个数据库连接分离出来  DETACH DATABASE "[alias name]"
* 创建表 
```SQL
CREATE TABLE database_name.table_name(
   column1 datatype  PRIMARY KEY(one or more columns),
   column2 datatype,
   column3 datatype,
   .....
   columnN datatype,
);
```
* 删除表 DROP TABLE database_name.table_name;
* 插入新数据    INSERT INTO TABLE_NAME [(column1, column2, column3,...columnN)]  VALUES (value1, value2, value3,...valueN);
* SELECT 用于从SQLite数据库中获取数据 SELECT column1, column2, columnN FROM table_name; 
*  也包含有一般的运算
*  WHERE语句 如果给定条件满足，则从表中返回特定的值
*  UPDATE语句 用于修改表中已有记录
```SQL
UPDATE table_name
SET column1 = value1, column2 = value2...., columnN = valueN
WHERE [condition];
``` 
* SQLite DELETE语句 删除表中已有记录
```SQL
DELETE FROM table_name
WHERE [condition];
```
* LIKE语句 %代表一个或者多个数字或字符 _代表单个数字或字符 **大小写不敏感**
* GLOB语句 *代表一个或者多个数字或字符 ?代表单个数字或字符 **大小写敏感**
* LIMIT语句 限制由 SELECT 语句返回的数据数量
```SQL
SELECT column1, column2, columnN 
FROM table_name
LIMIT [no of rows]
```
* ORDER BY语句 用来基于一个或多个列按升序或降序顺序排列数据 **ASC** 默认值，从小到大，升序排列 **DESC** 从大到小，降序排列


















