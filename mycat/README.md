### 分布式MySQL示例

1. 启动镜像 
```
dcoker-compose up -d
```

2. Attach Shell
连接某个mysql实例

3. 测试
```
# mysql -hmycat -uroot -P8066 -p
Enter password: 123456
mysql>use TESTDB;
mysql>insert into tb1(`name`) values('docker');
mysql>insert into tb1(`name`) values('php');
mysql>insert into tb1(`name`) values('mysql');
```
