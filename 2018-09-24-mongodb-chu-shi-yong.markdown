---
layout: post
title: "mongodb 初使用"
date: 2018-09-24 01:16:53 +0800
comments: true
categories: Java
---

## Java原生API操作MongoDB

本文主要介绍如何用原生api简易操作mongodb集群，

### 加入依赖
```xml
<dependency>
    <groupId>org.mongodb</groupId>
    <artifactId>mongo-java-driver</artifactId>
    <version>3.8.2</version>
</dependency>
```

使用集群方式连接Mongodb

### Java操作连接
```java
MongoCredential credential = MongoCredential.createCredential(MONGO_USRE, "admin", MONGO_PASSWD.toCharArray());
MongoClientOptions options = MongoClientOptions.builder().sslEnabled(false).build();
MongoClient mongoClient = new MongoClient(Arrays.asList(new ServerAddress("10.50.183.254", 27017),
                    new ServerAddress("10.50.184.74", 27017), new ServerAddress("10.50.182.164", 27017)), credential, options);

```

### 插入及更新
```
```