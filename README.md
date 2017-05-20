这是一个 Spring Boot 的入门项目，需要完成三个 Spring Boot 的 REST API 的编写。请按照项目验收测试中的要求完成。具体的实现方式可以参考 [Spring Boot Rest API](https://spring.io/guides/gs/rest-service/)。

## API

1. `GET /` 返回 "it works" 的文本信息并返回 http status code 200。
2. `GET /greeting` 返回 json 数据 `{"id": 1, "content": "Hello, World"}`，其中 `id` 为自增的整数。同时可以通过传入 `name` 的参数用来替换默认的 "World"，比如 `/greeting?name=User` 那么结果会返回 `{"id": 1, "content": "Hello, User"}`
3. `POST /greeting` 发送`{"name": "User"}` 的请求可以得到 `{"id": 1, "content": "Hello, User"}`，不过要注意这里所返回的 http code 为 201

## 项目运行要求

项目中使用了 java 8 以及 gradle。请确保本地安装了 java 8。

## 执行验收测试

在当前项目下执行 

    ./gradlew acceptanceTest
    
## 在本地启动 server

    ./gradlew bootRun
    
## 注意

请遵循目前的项目目录结构，在 `src/java` 下编写程序，目前项目所提供的依赖都已经能够满足项目功能的实现，任何额外的依赖都不会在 server 端的验收测试中使用。