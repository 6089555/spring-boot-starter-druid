# SPRING-BOOT-STARTER-DRUID

## 配置示例
```
druid:
    dataSource:
        driver-class: com.mysql.jdbc.Driver
        url: jdbc:mysql://localhost:3306/test
        username: root
        password: root
        initial-size: 1
        min-idle: 1
        max-active: 100
        test-on-borrow: true
        log-abandoned: true
        max-wait: 60000
        time-between-eviction-runs-millis: 60000
        min-evictable-idle-time-millis: 300000
        validation-query: SELECT 'x'
        test-While-Idle: true
        test-on-return: false
        pool-prepared-statements: false
        max-pool-prepared-statement-per-connection-size: 20
        filters: wall,mergeStat
        connection-properties: druid.stat.mergeSql=true;druid.stat.slowSqlMillis=5000;config.decrypt=false
    monitor:
        enabled: enabled
        druid-stat-view: /druid/*
        druid-web-stat-filter: /*
        allow: 127.0.0.1
        deny: 192.168.1.73
        login-username: admin
        login-password: 123456
        exclusions: '*.js,*.gif,*.jpg,*.png,*.css,*.ico,/druid/*'
        reset-enable: false
```
查看[Druid配置](https://github.com/alibaba/druid/wiki/DruidDataSource配置属性列表)