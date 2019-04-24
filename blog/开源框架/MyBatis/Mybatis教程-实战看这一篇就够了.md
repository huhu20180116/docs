# Mybatis教程-实战看这一篇就够了

原地址：https://blog.csdn.net/hellozpc/article/details/80878563

### 1.从JDBC谈起

#### 1.1.使用IDEA创建maven工程

![这里写图片描述](https://ws2.sinaimg.cn/large/006tNc79ly1g2drkmiyboj30tj0j9whr.jpg)

![这里写图片描述](https://ws3.sinaimg.cn/large/006tNc79ly1g2drl3yl46j30to0j70tl.jpg)

![这里写图片描述](https://ws3.sinaimg.cn/large/006tNc79ly1g2drmh23ndj30tn0jcwfy.jpg)

#### 1.2.引入mysql依赖包

```xml
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>5.1.32</version>
</dependency>
```

![](https://ws2.sinaimg.cn/large/006tNc79ly1g2driwxnq0j31du0m2tdg.jpg)

#### 1.3.准备数据

- 创建数据库：

```sql
CREATE DATABASE ssmdemo;
```

创建表：
DROP TABLE IF EXISTS tb_user;
CREATE TABLE tb_user (
id char(32) NOT NULL,
user_name varchar(32) DEFAULT NULL,
password varchar(32) DEFAULT NULL,
name varchar(32) DEFAULT NULL,
age int(10) DEFAULT NULL,
sex int(2) DEFAULT NULL,
birthday date DEFAULT NULL,
created datetime DEFAULT NULL,
updated datetime DEFAULT NULL,
PRIMARY KEY (id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

插入数据：
INSERT INTO ssmdemo.tb_user ( userName, password, name, age, sex, birthday, created, updated) VALUES ( ‘zpc’, ‘123456’, ‘鹏程’, ‘22’, ‘1’, ‘1990-09-02’, sysdate(), sysdate());
INSERT INTO ssmdemo.tb_user ( userName, password, name, age, sex, birthday, created, updated) VALUES ( ‘hj’, ‘123456’, ‘静静’, ‘22’, ‘1’, ‘1993-09-05’, sysdate(), sysdate());
--------------------- 


