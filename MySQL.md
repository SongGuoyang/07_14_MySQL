# 前言. 数据库

## 1.数据库的意义

> 数据库就是存放数据的仓库

想像一下, 在没有计算机之前, 我们如何统计人口数据的, 通常都是用纸和笔登记, 填写像这样的一张表格.

![人口统计表](http://image.brojie.cn/%E4%BA%BA%E5%8F%A3%E7%BB%9F%E8%AE%A1%E8%A1%A8.jpg)

再将这些表格按照一定的顺序整理

![一堆表](http://image.brojie.cn/%E4%B8%80%E5%A0%86%E8%A1%A8.jpg)

最后放到一个档案室里集中管理

![数据档案](http://image.brojie.cn/%E6%95%B0%E6%8D%AE%E6%A1%A3%E6%A1%88.jpg)

这个档案室实际上就是**一个存放数据的仓库**.

但是这种管理方式是非常低效的, 如果要从100万人中找出某一个人的信息, 是非常慢的.

数据库的产生实际上就是利用计算机, 方便高效的管理数据.

> 数据库是信息系统的重要组成部分

任何信息系统都离不开对数据的处理.

比如

- 新闻系统最核心的是一篇一篇的文章, 文章也就是数据
- 电商系统最核心的是商品, 商品也可以用数据来描述, 比如价格, 颜色, 重量...

## 2.数据库的基本概念

数据库最基本的组成单元就是一条一条数据记录, 这个就是**数据行**

为了让数据更加方便管理, 通常我们会使用表格来描述, 这个就是**数据表**

很多数据表放在一起就形成**数据库**

## 3.数据库的基本操作

> 添加操作

我们还是以人口统计为例. 

比如, 一个小孩出生了, 我们需要给小孩上户口. 

从数据库的角度就是将小孩的信息添加到数据库中保存起来. 

可能是保存在某一张表里(假设叫人口表)

一般都有哪些信息呢? 姓名, 性别, 籍贯, 身份证, 户口所在地...这些就是字段, 也就是表头

| id   | 姓名 | 性别 | 籍贯 | 户口所在地 |
| ---- | ---- | ---- | ---- | ---------- |
| 1    | 张三 | 男   | 武汉 | 北京       |
| 2    |      |      |      |            |
| 3    |      |      |      |            |
| 4    |      |      |      |            |

> 更新操作

又有一天, 小孩上大学了, 户口要迁移到学校, 需要修改户口所在地信息. 

从数据库的角度就是找到对应的小孩的信息, 更新户口所在地

> 删除操作

比如, 某个老人过世了, 需要删除这个老人的信息.

从数据库的角度就是找到对应的信息, 删除

> 查询操作

有的时候, 需要查询张三这个人的具体的信息, 怎么办?

每个人都有身份证号, 身份证号是唯一的. 每个人都不同, 可以根据身份证号做为查询条件, 查找张三的全部信息

# 一. MySQL概述

## 1.什么是MySQL

> 定义

MySQL是一种关系型数据库软件, 基于C/S架构

- 数据库: 存储数据的仓库
- 关系型: 数据与数据之间存在关系
- C/S架构: Client(客户端)和Server(服务端)

## 2.为什么学MySQL

对于后端工程师, 数据库是必备技能. 

对于前端工程师, 会一些数据库方面的知识

- 可以在接口联调的时候占主动
- 可以向全栈发展

MySQL是数据库中使用最广范的, 学了MySQL后再学其他的数据库也是非常容易的

![MySQL](http://image.brojie.cn/images/MySQL.jpg)

数据来源于: [StackOverflow2020调查报告](https://insights.stackoverflow.com/survey/2020)

## 3.如何理解关系型

> 关系型数据库有明确的**库/表/行**的关系

数据库由数据表组成

数据表由数据行(记录)组成

![1548489109447](http://image.brojie.cn/images/1548489109447.png)

## 4.MySQL的安装

### 1) 安装MySQL服务端

> 演示

### 2) 安装MySQL客户端

MySQL的客户端有很多种. 这里, 我主要使用的是Navicate

## 5.如何理解C/S架构

MySQL分为MySQL客户端和MySQL服务端

不管是客户端还是服务端, 本质上依然是一个程序

**服务端**: 提供服务的**程序**

**客户端**: 连接服务端执行操作的**程序**

> 演示

![1550452268907](http://image.brojie.cn/images/1550452268907.png)

![1550452347476](http://image.brojie.cn/images/1550452347476.png)

在命令行中输入`mysql -uroot -p`, 连接服务端, 因此, 当前的这个窗口就是一个MySQL的客户端

> 思考

MySQL主要操作是在哪些完成的? 客户端!

# 二. MySQL基本操作

一般MySQL操作都是在操作MySQL客户端

这里, 我们可以使用一些图形化的软件, 如Navicate/MySQL-Front. 

如果需要操作MySQL, 需要先使用MySQL客户端连接到服务端

![1548497143947](http://image.brojie.cn/images/1548497143947.png)

## 1.客户端连接与基本操作

### 1) 连接数据库

![1550700902461](http://image.brojie.cn/images/1550700902461.png)

点击后弹出如下窗口

![1550701001417](http://image.brojie.cn/images/1550701001417.png)

### 2) 创建数据库

### 3) 选择数据库

![1550701067184](http://image.brojie.cn/images/1550701067184.png)

两种操作

- 双击
- 右键->打开数据库

### 3) 建库建表

看演示

## 2.SQL概念(了解)

### 1) 什么是SQL

Structured Query Language 结构化查询语言

### 2) SQL的作用

- 是一种所有关系型数据库的查询规范, 不同的数据库都支持
- 通用的数据库操作语言, 可以用在不同的数据库中

### 3) SQL语句分类

- Data Definition Language(DDL数据定义语言) 如: 建库, 建表
- Data Manipulation Language(DML 数据操纵语言) 如: 对表记录的增/删/改
- Data Query Language(DQL 数据查询语言) 如: 对表的查询操作
- Data Control Language(DCL 数据控制语言) 如: 对用户权限的设置

使用频率

CURD(增删改查)占到了数据库操作80%

查询占到CURD的80%

### 4) MySQL的语法

- 每条语句以分号结尾
- SQL中不区分大小写, 推荐关键字大写以区分

# 三. 数据类型

## 0.前言

在现实世界中, 数据的种类有很多, 

比如, 人的姓名(字符), 人的年龄(整型), 人的身高(小数), 出生日期(日期)

而MySQL就是用来保存这些数据的, 所以在 MySQL中, 将数据分为三大类: 

- 数值型
- 字符串
- 日期与时间

> 学习目的

通过学习, 大概了解怎么选择合适的数据类型

![img](http://image.brojie.cn/wpsFC64.tmp.jpg)

## 1.数值--整型

| 类型 | 名称     | 说明                 | 无符号范围   | 有符号范围   |
| ---- | -------- | -------------------- | ------------ | ------------ |
| 整型 | tinyint  | 微整型, 占8位二进制  | 0~255        | -127~128     |
|      | smallint | 小整型, 占16位二进制 | 0~65535(6万) | -32767~32768 |
|      | int      | 整型                 | 0~42亿       |              |
|      | bigint   | 大整型               | 0~200亿亿    |              |

> 选型

一个人的年龄:  tinyint

小型blog的序号: smallint

大学一个学校的学生序号: int

大型电商网站的商品表的序号: int

马云的资产: bigint

> 说明

在mysql中, 默认的整型是带符号的, 如果要定义无符号整型, 需要加上`unsigned`

> 示例

```SQL
CREATE TABLE `t_int` (
    age tinyint unsigned,
    stu_sn smallint unsigned,
    goods_sn int unsigned,
    mayun bigint
);
```

## 2.数值--小数

小数分为

- 浮点
  - 单精度
  - 双精度
- 定点

浮点型的数据不精确, 所以一般表示价格, 我们使用定点型

| 类型 | 名称         | 说明                                             |
| ---- | ------------ | ------------------------------------------------ |
| 小数 | float(m,d)   | m(精度), 表示总位数, d(标度), 表示小数点后的位数 |
|      | double(m,d)  | m(精度), 表示总位数, d(标度), 表示小数点后的位数 |
|      | decimal(m,d) | m(精度), 表示总位数, d(标度), 表示小数点后的位数 |

> 选型

距离: 3.4 km float(10,2) 

人的体重: 80.5kg  float(5,2)

价格: 9.9 RMB decimal(10,2)

> 示例

```sql
CREATE TABLE `t_float` (
    distance float(10,2),
    weight float(5,2),
    price decimal(10,2)
);
```

## 3.字符串

| 类型   | 名称           | 说明                                        |
| ------ | -------------- | ------------------------------------------- |
| 字符型 | char(M)定长    | 无论使用几个字符都占满全部, 范围0~255字符   |
|        | varchar(M)变长 | 使用几个字符就占用几个, 理论范围0~65535字符 |
|        | text           | 允许长度 0~65535 字节                       |
|        | enum(集合)     | 枚举, 集合表示选项, 以逗号隔开              |

> 选型

char类型: 固定长度, 一般用于存储固定长度的字符串, 如

- 手机号 char(11)
- 通过md5加密后的密码值char(32)

varchar类型: 可变长度, 存储长度不确定的字符字符串, 如

- 姓名 varchar(16)
- 邮箱 varchar(255)

text类型: 存储大段内容, 如

- 文章内容 text

enum类型: 单选, 如

- 性别

> 说明

char与varchar的区别

- char是固定的长度 char(5) 保存 abc, 实际占用的空间5个
- varchar最大长度 varchar(5)保存abc, 实际占用的空间3个

varchar用多少就占多少

> 示例

```sql
CREATE TABLE `t_char` (
    phone char(11),
    password char(32),
    name varchar(16),
    email varchar(255),
    content text,
    sex enum('男','女')
);
```

> 说明

char(M)与varchar(M)中的M表示的字符数

## 4.日期与时间

| 类型 | 名称      | 说明                                        |
| ---- | --------- | ------------------------------------------- |
| 日期 | date      | 范围1000-01-01~9999-12-31                   |
|      | datetime  | 范围1000-01-01 00:00:00~9999-12-31 23:59:59 |
|      | timestamp | 从1970年开始至今的秒数                      |

> 选型

出生日期: date

商品抢购的开始结束时间: datetime

文章的创建更新时间: timestamp(时间戳)

> 说明

时间戳: 从1970年1月1日0时0分0秒到当前时间的秒数(整数)

一般时间类型更常见的是保存时间戳, 时间戳就是一个整型数, 为什么保存时间戳呢?

1. 效率更高
2. 方便处理

> 示例

```sql
CREATE TABLE `t_time` (
    birthday date,
    start_time datetime,
    end_time datetime,
    created_time timestamp
);
```



# 六. 字段属性

字段属性又叫字段约束, 通常用来限定(约束)当前列

- 能否为空
- 默认值

## 1.能否为空

如果需要当前字段不能为空, 默认情况下是可以为空的

> 关键词

not null

> 语法

```sql
CREATE TABLE `表名` (
    字段 字段类型 not null
);
```

> 示例

```sql
CREATE TABLE `t_null` (
    id int,
    name varchar(16) not null
);
```



## 2.默认值

有些情况下，我们希望某个字段拥有默认值，比如

- 性别的字段，拥有默认值为“男”
- 籍贯的字段，拥有默认值为“汉”

> 关键词

default

> 语法

```sql
CREATE TABLE `表名` (
    字段 字段类型 default 默认值
);
```



> 示例

```sql
CREATE TABLE `t_default` (
    name varchar(16),
    sex enum('男','女') default '男'
);
```

## 3.主键

如果我们可以通过某一列进行唯一的标识每一条记录，我们就可以把这个字段当做主键

> 关键词

primary key

> 语法

```sql
CREATE TABLE `表名` (
    字段 字段类型 primary key
);
```

## 4.自增

如果数据表中的某个字段，需要进行自动增长，我们可以将其定义为自动增长, **一般自增跟主键连用**

> 关键词

auto_increment

> 语法

```sql
CREATE TABLE `表名` (
    字段 字段类型 primary key auto_increment
);
```

> 示例

```sql
CREATE TABLE `t_primary` (
    id int primary key auto_increment
);
```

## 5.备注

在创建字段时, 一般需要给一定的说明

> 关键词

comment

> 语法

```sql
CREATE TABLE `表名` (
    字段 字段类型 字段属性 comment '备注'
);
```

> 示例

```sql
CREATE TABLE `t_comment` (
    id int primary key auto_increment comment '主键',
    name varchar(16) not null comment '姓名'
);
```

> 完整的建表语句

```sql
CREATE TABLE `表名` (
    字段1 字段类型1 字段属性1 字段属性2 字段属性3,
    ...
);
```

# 七. 综合建表案例

## 1.文章表blog

> 分析

blog表需要哪些字段

- 主键id
- 作者(author)
- 标题(title)
- 内容(content)
- 浏览数(click)
- 评论数(comment)
- 发布时间(publish_time)

```sql
CREATE TABLE `blog` (
  `id` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',
  `title` varchar(255) NOT NULL DEFAULT '' COMMENT '标题',
  `content` text NOT NULL COMMENT '内容',
  `author` varchar(32) NOT NULL DEFAULT '' COMMENT '作者',
  `click` int(11) NOT NULL DEFAULT '0' COMMENT '浏览数',
  `comment` smallint(6) NOT NULL DEFAULT '0' COMMENT '评论数',
  `publish_time` date DEFAULT NULL COMMENT '发布日期',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```



## 2.商品表goods

> 分析

goods表需要哪些字段

- 主键id
- 分类id(cate_id)
- 商品名称(goods_name)
- 本店价格(shop_price)
- 市场价格(market_price)
- 商品数量(goods_number)
- 点击数(click)

```sql
CREATE TABLE `goods` (
    id int unsigned primary key auto_increment comment '主键',
    cate_id int not null comment '所属分类',
    goods_name varchar(255) not null comment '商品品称',
    shop_price decimal(10,2) not null default 0 comment '本店价格',
    market_price decimal(10,2) not null default 0 comment '市场价格',
    goods_number int not null comment '商品数量',
    click int not null default 0 comment '点击数'
);
```



## 3.学生表stu

> 分析

stu表需要哪些字段

- 主键id
- 学号(sn) 
- 姓名(name)
- 性别(sex) enum
- 学科(subject)
- 身高(height) float

```sql
CREATE TABLE `stu` (
    id int unsigned primary key auto_increment comment '主键',
    sn char(8) unique not null comment '学号',
    name varchar(32) not null comment '姓名',
    sex enum('男', '女') not null default '男' comment '性别',
    subject varchar(16) not null comment '学科',
    height float(3,2) not null comment '身高'
);
```

# 八. 数据的写操作(重点)

## 0.前言

MySQL最主要的功能是<u>**管理数据**</u>, 也就是`增/删/改/查`, 也叫`CURD`, 从大的方面划分就是**写操作**和**读操作**

首先, 我们来学习**写操作**

## 1.添加操作

### 1) 基本用法

把握3点

1. 插入哪张**表**?
2. 插入表的哪些**列**(字段)?
3. 这些列的**值**?

> 语法

```sql
INSERT INTO `表名`
(`字段1`, ... `字段n`)
VALUES
(值1, 值2, 值n)
```

> 示例一. 插入单条记录

```sql
# 先选择db1数据库
USE `db1`;
# 向t1表中添加一条数据
INSERT INTO `t1`
(`id`, `name`, `age`)
VALUES
(1, 'xiaoming', 20);
```

如何查看数据是否添加成功?

先了解一个基本的查询操作

```sql
# 查询表中的所有记录
select * from `表名`;
```

> 示例二. 一次插入多条记录

```sql
# 向t1表中一次添加多条记录
INSERT INTO `t1`
(`id`, `name`, `age`)
VALUES
(2, 'xiaomei', 18),
(3, 'xiaoqiang', 22);
```

一个() : 代表一条记录

多个()使用,隔开

> 扩展

如果已经在db1数据库下, 不用执行`USE命令`, 也可以显式的指定库名, 如

```sql
INSERT INTO db1.t1
(`id`, `name`, `age`)
VALUES
(1, 'xiaoming', 20);
```



### 2) 允不允许只插入部分字段和值?

> 尝试

```sql
INSERT INTO `student`
(`name`, `age`)
VALUES
('xiaomei', 18);
```

结论: _____________

### 3) 允不允许不写字段?

> 尝试

```sql
INSERT INTO `student`
VALUES
('laowang', 30);
```

> 尝试

```sql
INSERT INTO `student`
VALUES
(null, 'laowang', 30);
```

结论: _________

### 4) 添加案例

- 超出整型范围

```sql
INSERT INTO `t_int` (age) VALUES (300);
```

- 浮点型精度丢失问题

```sql
INSERT INTO `t_float` VALUES (12345678.12, 123.12, 12345678.12);
```

- 插入中文数据

```sql
INSERT INTO `t_char` (name) VALUES ('小明');
```

- 如果插入的字符串超过长度, 会怎样?

```sql
INSERT INTO `t_char` (phone) VALUES ('130123456789');
```

- 如果插入的值不在enum的选型类, 会怎样?

```sql
INSERT INTO `t_char` (sex) VALUES ('女博士');
```

- 如果字段类型是字符型, 插入的数据是整型或者小数型会怎样?

```sql
INSERT INTO `t_char` (phone) VALUES (13012345678);
INSERT INTO `t_char` (phone) VALUES (123456789.1);
```

- 如果字段不能为null, 但是添加的时候没有指定会怎样?

```sql
INSERT INTO `t_null` (id) VALUES (1);
```

设置了not null的字段, 在插入数据时必须出现在字段列表中

- 如果设置了默认值, 但是添加的时候没有指定会怎样?

```sql
INSERT INTO `t_default` (name) VALUES ('xiaoming');
```

> 添加案例小结
>

- 插入数据的类型最好与要求的类型一致
- 插入的数据必须在有效范围内
- 插入的数据为null时给默认值
- 自增会在原来的基础上+1

## 2.修改操作

4点

1. 修改哪张**表**?
2. 修改表的哪些**列**(字段)?
3. 这些列的**值**?
4. 条件

> 语法

```sql
UPDATE `表名`
SET
`字段1`=值1,
`字段2`=值2,
...
WHERE 条件
```

> 示例

```sql
UPDATE `student`
SET
`name`='xiaoming-new'
WHERE `id`=1;
```

> 演示

## 3.删除操作

2点

1. 删除哪张表?
2. 删除哪些行?

> 语法

```sql
DELETE FROM `表名` WHERE 条件
```

> 示例

```sql
DELETE FROM `student` WHERE `id`=3;
```

> 演示

# 九. 查询--基本查询

相对于写操作, 读操作(查询操作)使用的更为频繁, 大部分的业务都体现在读操作上, 内容比较多

我们先学习基本查询

## 1.基本用法

### 1) 基本查询

3点:

1. 查哪张**表**的数据?
2. 查哪些**列**的数据?
3. 条件

> 语法

```sql
SELECT 字段1, 字段2, ...字段n 
FROM 表名
[WHERE 条件]
```

> 示例1--查询指定的列

```sql
# 查询t1表中的name和age字段
SELECT `name`, `age` FROM `t1`;
```

> 演示



> 示例2--查询所有的列

```sql
# 查询t1表中的所有数据
SELECT * FROM `t1`;
```

- `*` : 表示所有字段

> 演示



> 示例3--根据条件查询

```sql
# 查询xiaomei的年龄
SELECT `age` FROM `t1` WHERE `name`='xiaomei';
```

> 演示



### 2) 别名

可以给指定的列取一个别名, 一般用于多表查询中

> 语法

```sql
SELECT 字段1 as 别名1, 字段2 as 别名2 FROM 表名 as 表别名
```

其中, as关键字可以省略

> 示例

```sql
SELECT `name` as `username` FROM `t1` as stu;
```

> 演示



## 2.查询模型

### 1) 基本点

3个点

1. 列当作变量
2. 列可以参与计算
3. where条件判断真假

> 如何理解

逐行比较, 当where条件为真的时候, 把列(变量)的值取出来

> 示例

```sql
SELECT name, age FROM `student`;
```

> 演示



> 示例2

```sql
# 查询本店价比市场价低多少(计算差价)
SELECT market_price - shop_price FROM `goods`;
```

> 演示



### 3) where条件

MySQL中常用的运算符如下表:

| 运算符              | 说明                                                         |
| ------------------- | ------------------------------------------------------------ |
| >, <, <=, >=, =, <> | <>表示不等于, 也可以使用!=                                   |
| BETWEEN...AND       | 在某个范围内, between 100 and 200, 包含100和200, 闭区间[100, 200] |
| IN (1,2, ... n)     | 集合表示多个值，使用逗号分隔                                 |
| LIKE                | 模糊查询                                                     |
| is null             | 查询某一列为null                                             |
| is not null         | 查询某一列不为null                                           |

| 逻辑运算符   | 说明                                  |
| ------------ | ------------------------------------- |
| and 或者 &&  | 与， SQL 中建议使用前者，后者并不通用 |
| or 或者 \|\| | 或                                    |
| not 或者 !   | 非                                    |

| 通配符 | 说明             |
| ------ | ---------------- |
| %      | 匹配任意多个字符 |
| _      | 匹配一个字符     |

## 3.查询案例

以商品表为例, 做如下查询练习

1.1 查询主键id为32的商品

```sql
SELECT * FROM `goods` WHERE `id`=32;
```

1.2 不属第3栏目的所有商品id和名称

```sql
SELECT `id`, `goods_name`, `cate_id`
FROM `goods`
WHERE `cate_id` != 3;
```

1.3 本店价格高于3000元的商品

```sql
SELECT `goods_name`, `shop_price`
FROM `goods`
WHERE `shop_price` > 3000;
```

1.4 本店价格低于或等于100元的商品

```sql
SELECT `goods_name`, `shop_price`
FROM `goods`
WHERE `shop_price` <= 100;
```

1.5 取出第4栏目或第11栏目的商品(使用or或者使用in)

```sql
# 使用or
SELECT `goods_name`, `cate_id`
FROM `goods`
WHERE `cate_id`=4 or `cate_id`=11;

# 不使用or
SELECT `goods_name`, `cate_id`
FROM `goods`
WHERE `cate_id` in (4, 11);
```

1.6 取出100<=本店价格<=500的商品(使用and或者between)

```sql
# 使用and
SELECT `goods_name`, `shop_price`
FROM `goods`
WHERE `shop_price` >= 100 and `shop_price` <= 500;

# 不使用and
SELECT `goods_name`, `shop_price`
FROM `goods`
WHERE `shop_price` between 100 and 500;
```

1.7 取出不属于第3栏目且不属于第11栏目的商品(使用and或使用not in分别实现)

```sql
# 使用and
SELECT `goods_name`, `cate_id`
FROM `goods`
WHERE `cate_id` != 3 and `cate_id` != 11;

# 使用 not in
SELECT `goods_name`, `cate_id`
FROM `goods`
WHERE `cate_id` not in (3, 11);
```

1.8 取出第3个栏目下面价格<1000或>3000,并且点击量>5的商品

```sql
SELECT `goods_name`, `cate_id`, `shop_price`, `click_count`
FROM `goods`
WHERE `cate_id`=3
and (`shop_price` < 1000 or `shop_price` > 3000)
and `click_count` > 5;
```

1.9 取出名字以"诺基亚"开头的商品

```sql
SELECT `goods_name`
FROM `goods`
WHERE `goods_name` LIKE '诺基亚%';
```

1.10 取出名字为"诺基亚Nxx"的手机

```sql
SELECT `goods_name`
FROM `goods`
WHERE `goods_name` LIKE '诺基亚N__';
```

# 十. 进阶查询操作(select子句)

## 0.前言

MySQL除了能做基本的条件查询操作外, 还可以用来过滤数据, 比如分组统计, 排序等

通过, SELECT的子句, 可以完成复杂的操作, 除了where子句, 还有如下4个, 一般称select 子句

- group by
- having
- order by
- limit

> 注意

子句的顺序不能颠倒, 如下

```sql
SELECT 字段 FROM 数据表  
where子句  
group by子句  
having子句  
order by 子句  
limit 子句;
```

## 1.group by子句

分组的目的是为了统计, 因此分组通常和聚合函数连用

> 聚合函数

- count: 计算总数
- sum: 求和
- max: 最大值
- min: 最小值
- avg: 平均值

> 聚合函数用法示例

查出最贵的商品价格

```sql
SELECT max(shop_price) FROM `goods`;
```

查出最便宜的商品的价格

```sql
SELECT min(shop_price) FROM `goods`;
```

查询该店所有商品的库存总量

```SQL
SELECT sum(goods_number) FROM `goods`;
```

查询所有商品的平均价

```sql
SELECT avg(shop_price) FROM `goods`;
```

查询该店一共有多少种商品

```sql
SELECT count(*) FROM `goods`;
```

```sql
SELECT sex, count(*) FROM `stu` GROUP BY `sex`; // 更推荐
SELECT sex, count(sex) FROM `stu` GROUP BY `sex`;
```

> 练习

需求: 统计每个栏目下最贵的商品

思路:

- 第一步: 按照栏目(cate_id)对所有的数据进行分组
- 第二步: 使用聚合函数求最大值

> 分组统计

第一步: 分组

```sql
SELECT cate_id FROM goods group by cate_id;
```

第二步: 统计

```sql
SELECT `cate_id`, max(shop_price)
FROM `goods`
GROUP BY `cate_id`;
```



## 2.having子句

having跟where一样, 用来做**条件的判断**和**数据的筛选过滤**

在MySQL中，我们可以使用where进行条件的过滤, 也可以使用having.

> 示例

```sql
# 可以用where也可以用having
SELECT * FROM `t1` WHERE `age` > 18;
SELECT * FROM `t1` HAVING `age` > 18;
```

> 演示

where和having的区别

- where中的条件是`表字段`
- having中的条件是`结果集`

> 示例

查询差价>200的商品信息

```sql
# 使用where
SELECT `goods_name`,  market_price-shop_price as `chajia`
FROM `goods`
WHERE market_price-shop_price > 200;
```

```SQL
# 使用having
SELECT `goods_name`,  market_price-shop_price as `chajia`
FROM `goods`
HAVING chajia > 200;
```

> group和having综合示例

查询该店每个栏目下面积压的总货款

```sql
SELECT `cate_id`, sum(goods_number*shop_price) as `jiya`
FROM `goods`
GROUP BY `cate_id`;
```

查询积压货款>1000的栏目

```sql
SELECT `cate_id`, sum(goods_number*shop_price) as `jiya`
FROM `goods`
GROUP BY `cate_id`
HAVING `jiya`>1000;
```

> 结论

1. having通常和group by连用
2. having的判断条件是结果集



## 3.order by子句

order by就是实现对数据的排序操作. 一共有两种情况:

- 一种是**升序**排列(asc)
- 一种是**降序**排列(desc)

应用场景:

各种排序场合,如新闻按点击量排序, 商品按价格排序, 文章按更新时间排序等

> 示例

按价格由高到低排序

```sql
SELECT `goods_name`, `shop_price`
FROM `goods`
ORDER BY `shop_price` desc;
```

> 多个字段同时排序

按栏目由低到高排序,栏目内部按价格由高到低排序

```sql
SELECT `cate_id`, `goods_name`, `shop_price`
FROM `goods`
ORDER BY `cate_id` asc, `shop_price` desc;
```



## 4.limit 子句

limit子句用于限定数目

应用场景:

最新的5遍文章, 成绩倒数3名的学生, 点击量最高的10件商品

分页!!!

limit子句有两种语法

> 语法

```sql
# 带一个参数, 表示显示多少条
limit N
# 带二个参数, 表示从N条(偏移量)开始, 显示M条
limit N,M
```

> 示例

查询价格最高的前三的商品

```sql
SELECT `goods_name`, `shop_price`
FROM `goods`
ORDER BY `shop_price` DESC
LIMIT 3;
```

> 分页示例

每页5件商品, 显示第2页的数据

```sql
SELECT `id`, `goods_name`
FROM `goods`
LIMIT 5,5;
```

分页公式: 偏移量 = (当前页码-1) * 每页显示数

> 尝试

每页3件商品, 显示第4页的数据

SQL: _________

# 十一. E-R实体关系模型

## 1.什么是实体

E: entity(实体)

R: relation(关系)

### 1) 实体

> 实体的定义
>
> ​	客观存在并相互区别的一个事物称为实体（Entity）

举例: 如一个学生、一件商品、一个部门、一个课程, **相当于数据表中一条记录**

### 2) 实体属性

> 属性的定义
>
> ​	实体的某些特性称为实体的属性（Attribute），一个实体可以拥有多个属性

举例: 如学生有学号、姓名、性别、出生日期等, **相当于字段**

![image-20210127133809634](http://image.brojie.cn/image-20210127133809634.png)

### 3) 实体集

> 定义
>
> ​	实体的集合, 相当于一张表

## 2.关系

表与表之间的关系一共有4种

- 一对一
- 一对多
- 多对一
- 多对多

### 1) 一对一关系

> 定义

一张表的**一条记录**对应另一张表的**一条记录**

> 举例

看如下两张表

用户表(user)和用户详情表(user_info)

user表中的一条记录, 比如xiaoming, 对应的user_info的一条记录

> 关联条件

user.id=user_info.user_id

### 2) 一对多关系

> 定义

一张表的**一条记录**对应另一张表的**多条记录**

> 举例

看如下两张表

用户表(user)和文章表(article)

user表中的一条记录, 比如xiaoming, 对应的article中的多条记录

说明: 一个用户可以**拥有**(has)多篇文章 hasMany

> 关联条件

user.id=article.user_id

### 3) 多对一关系

> 定义

一张表的**多条记录**对应另一张表的**一条记录**

> 举例

看如下两张表

用户表(user)和国家表(country)

user表中的多条记录, 对应的country中的一条记录

说明: 多个用户**属于**(belongsto)一个国家

> 关联条件

user.country=country.id

### 4) 多对多关系

> 定义

表A的**一条记录**对应表B的**多条记录**

同时, 表B的**一条记录**也对应表A的**多条记录**

> 举例

看如下两张表

用户表(user)和角色表(role)

说明: 一个用户拥有多个角色, 一个角色也拥有多个用户

> 关联条件

建立中间表, 将多对多转换成两个一对多处理



父表: 一的那方叫做父表

子表: 多的那方叫做子表

在子表中建立一个字段, 让这个字段=父表的id, 那么在子表中建立的这个字段就叫做外键

