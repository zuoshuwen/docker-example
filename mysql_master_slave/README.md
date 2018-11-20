### 主从配置

1. 启动镜像 
```
dcoker-compose up -d
```

2. 创建用户
```
CREATE USER 'slave'@'%' IDENTIFIED BY '123456';
GRANT REPLICATION SLAVE, REPLICATION CLIENT ON *.* TO 'slave'@'%';
```
3. 在master上执行 
```
show master status;
```
记下 File、Position的值填入步骤4

4. 在slave上执行 
```
CHANGE MASTER TO master_host = 'mysql_master',
master_port = 3306,
master_user = 'slave',
master_password = '123456',
master_log_file = 'mysql-bin.000004',
master_log_pos = 986;
start slave;
```

5. 测试