Java Spring Boot Rest Api Demo
==============================

## 如何使用SpringBoot来定义RestApi

```
brew install httpie
./mvnw package
java -jar target/demo-0.0.1-SNAPSHOT.jar
```

```
http POST http://localhost:8080/api/messages text=aaa
http POST http://localhost:8080/api/messages text=bbb

http POST http://localhost:8080/api/messages text=aa##bb

http GET http://localhost:8080/api/messages

http GET http://localhost:8080/api/messages/0
```

## 部署说明
### 前置条件

[Heroku账号](https://signup.heroku.com/login)

Java8

Maven

### 操作步骤

1.[安装Heroku本地服务](https://devcenter.heroku.com/articles/getting-started-with-java#set-up)

2.本地运行Rest API服务：
```
$ git clone git@github.com:nockyQ/java-spring-boot-rest-api-demo.git
$ cd java-spring-boot-rest-api-demo
$ ./mvnw install
$ heroku local:start
```
App将会运行于http://localhost:5000。 如果还需要使用数据库的话，确保当前目录有.env文件且包含JDBC链接，示例如下：
```
JDBC_DATABASE_URL=jdbc:postgresql://localhost:5432/java_database_name
```
3.发布服务：
```
$ heroku create
$ git push heroku master
$ heroku open
```
### 参考文档
https://devcenter.heroku.com/articles/getting-started-with-java

 
