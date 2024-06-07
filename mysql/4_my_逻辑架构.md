## 1.逻辑架构刨析

### 1.1 服务器处理客户端请求

![image-20240530111937314](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530111937314.png)



![image-20240530112101537](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112101537.png)

### 1.2 Connectors

![image-20240530112900690](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112900690.png)

### 1.3 第1层：连接层

![image-20240530112146970](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112146970.png)

![image-20240530112230870](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112230870.png)

### 1.4 第2层：服务层

![image-20240530112254556](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112254556.png)

![image-20240530112324327](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112324327.png)

![image-20240530112341323](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112341323.png)

![image-20240530112417856](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112417856.png)

### 1.5 第3层：引擎层

![image-20240530112432522](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112432522.png)

![image-20240530112502634](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112502634.png)

### 1.6 存储层

![image-20240530112522698](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112522698.png)

![image-20240530112550082](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530112550082.png)

### 1.7 小结

![image-20240530113533377](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530113533377.png)

## 2.SQL执行流程



### 2.1 MySQL 中的 SQL执行流程

![image-20240530114203658](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530114203658.png)



![image-20240530114316816](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530114316816.png)

![image-20240530114403970](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530114403970.png)

![image-20240530114453681](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530114453681.png)

![image-20240530114558722](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530114558722.png)

![image-20240530124218495](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124218495.png)

![image-20240530124237653](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124237653.png)

![image-20240530124257093](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124257093.png)

![image-20240530124321105](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124321105.png)

![image-20240530124336640](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124336640.png)

![image-20240530124408903](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124408903.png)

![image-20240530124424688](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124424688.png)

![image-20240530124441902](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124441902.png)

![image-20240530124500726](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124500726.png)

![image-20240530124529357](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124529357.png)

![image-20240530124558620](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124558620.png)

![image-20240530124622784](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124622784.png)

### 2.2 MySQL8中SQL执行原理

![image-20240530124845405](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124845405.png)

#### \1. 确认profiling 是否开启

![image-20240530124901443](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530124901443.png)

#### \2. 多次执行相同SQL查询

![image-20240530125342049](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530125342049.png)

#### \3. 查看profiles

![image-20240530125356271](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530125356271.png)

#### \4. 查看profile

![image-20240530125417562](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530125417562.png)

![image-20240530125442800](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530125442800.png)



### 2.3 MySQL5.7中SQL执行原理



#### \1. 配置文件中开启查询缓存



#### \2. 重启mysql服务



#### \3. 开启查询执行计划



#### \4. 执行语句两次：



#### \5. 查看profiles



#### \6. 查看profile



### 2.4 SQL语法顺序

![image-20240530131721796](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530131721796.png)

### 2.5 Oracle中的SQL执行流程(了解)

![image-20240530131640773](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530131640773.png)

![image-20240530131800439](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530131800439.png)

![image-20240530131825784](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530131825784.png)

![image-20240530131853224](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530131853224.png)



### 3.数据库缓冲池(buffer pool)

![image-20240530223713457](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530223713457.png)

## 3.1 缓冲池 vs 查询缓存

#### 1.缓冲池

![image-20240530223925608](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530223925608.png)

![image-20240530224038674](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224038674.png)

#### 2.查询缓存

![image-20240530224207662](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224207662.png)

### 3.2 缓冲池如何读取数据

![image-20240530224246026](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224246026.png)

![image-20240530224409977](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224409977.png)

### 3.3 查看/设置缓冲池的大小

![image-20240530224512362](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224512362.png)

![image-20240530224559552](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224559552.png)



### 3.4 多个Buffer Pool实例

![image-20240530224630140](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224630140.png)

![image-20240530224804677](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224804677.png)

### 3.5 引申问题

![image-20240530224929429](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530224929429.png)

![image-20240530225210546](C:\Users\hao\AppData\Roaming\Typora\typora-user-images\image-20240530225210546.png)