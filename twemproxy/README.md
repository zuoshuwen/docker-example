### 分布式缓存示例

1. 启动镜像
```
dcoker-compose up -d
```

2. Attach Shell twemproxy实例
登进后执行
```
/usr/local/sbin/twemproxy/sbin/nutcracker -d -c /usr/local/sbin/twemproxy/conf/nutcracker.yml -o /usr/local/sbin/twemproxy/log/nutcracker.log
```

3. Attach Shell redis实例
登进后执行
```
# redis-cli -h twemproxy -p 6666
twemproxy:6666> set 3234 zsw
```