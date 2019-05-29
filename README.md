How to make eureka server
====================

### 1.Add dependency.
```xml
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>

<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-config</artifactId>
  <version>2.1.1.RELEASE</version>
</dependency>
```

### 2.Add annotation in run class
```java
@EnableEurekaServer
```

### 3.Add posts to application.properties
Set port, turn off registration for simple test.
```java
server.port=8761
eureka.client.register-with-eureka=false
eureka.client.fetchRegistry=false
eureka.client.server.waitTimeInMsWhenSyncEmpty=0
```

### 4.Every client you must add annotation ahead run method
```java
@EnableDiscoveryClient
```

### 5.And dependency to pom.xml
```java
<dependency>
   <groupId>org.springframework.cloud</groupId>
   <artifactId>spring-cloud-starter-eureka</artifactId>
</dependency>
```
