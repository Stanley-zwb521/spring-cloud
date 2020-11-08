# Tutorial
Full stack training, assignment: https://github.ibm.com/lanzejun/q3-spring-cloud

## Spring cloud

### 1. Spring Boot 2.x学习
    Spring Boot 概述
    利用Spring Boot简化应用程序开发
    Spring Boot中的核心组件
        Spring Boot Starters
            Spring Boot Starter的父POM
        Spring Boot auto-configuration
        启用 Spring Boot auto-configuration
        Spring Boot CLI
        Spring Boot Actuator
    搭建 Spring Boot 开发环境
        利用Maven搭建Spring Boot
        利用Gradle搭建Spring Boot
    开始我们的第一个Spring Boot应用程序
        使用Spring在线界面初始化项目
        使用Spring STS IDE编辑器初始化项目
    实现REST服务
    Spring Boot 2.x中的新特性
    小结

### 2. 定制Spring Boot的Auto-Configuration
    理解auto-configuration
        学习auto-configuration如何工作的
    定制Spring Boot
        利用Spring Boot properties进行定制
        替换已生成的Bean
        禁用特定的auto-configuration类
        修改库的依赖
    基于属性的配置外部化
        属性的覆盖（overridden）顺序
        重命名application.properties文件
    外部配置应用程序属性
        使用@EnableConfigurationProperties注解
    基于日志记录的调优
        输出日志记录
    使用YAML配置文件
        YAML里面的层级属性
        单一YAML文件中的多个profiles属性
    定制应用程序错误页面
    小结

### 3. Spring CLI和Actuator
    开始使用Spring Boot CLI
        安装Spring Boot CLI
            从安装文件中手动安装Spring Boot CLI
            使用SDKMAN!安装Spring Boot CLI
            利用OSX Homebrew安装Spring Boot CLI
                使用MacPorts安装Spring Boot CLI
                使用Command-line安装Spring Boot CLI
    使用Spring Boot CLI初始化项目
    Spring Boot Actuator介绍
        启用Spring Boot的Actuator
        分析Actuator的接口
        显示配置细节
        利用接口显示指标
        显示应用程序信息
        关闭应用程序
        自定义Actuator
            启用或禁用某个Actuator接口
            更改接口ID
            更改Actuator接口的灵敏度
            编写自定义健康指标
        创建一个自定义接口
    对Actuator接口进行安全控制
    小结

### 4. Spring Cloud和配置操作
    云的应用程序架构
        微服务架构
            微服务的优点
            微服务面临的挑战
    Spring Cloud简介
        构建云和微服务应用
        Spring Cloud的使用
    配置Spring Cloud应用程序
    创建配置生成器———Spring Cloud Config Server
        搭建项目和依赖
    实现Cloud Config Server
        配置application.properties文件
        Creating a Git repository as configuration storage
            Running your configuration application
    Configuring multiple repositories using patterns
        Authentication
        Force-pull property
    Creating the configuration consumer Spring Cloud Config client
    小结

### 5. Spring Cloud Netflix and Service Discovery
    Introduction to Spring Cloud Netflix
    The need for Service Discovery in the microservices architecture
    Implementing Service Discovery &#x2013; Eureka Server
        The Maven build configuration file
        The Gradle build configuration file
        Enabling the Eureka server as a Discovery Service server
    Implementing Service Discovery &#x2013; Eureka clients
        Adding the Maven dependencies configuration
        The Gradle build configuration
    Registering a client with Eureka
        Consuming the REST service
        Using EurekaClient
            Using DiscoveryClient
            Client-side load balancing using Netflix Ribbon
        Using the registry-aware Spring Cloud Netflix FeignClient client
    小结

### 6. Building Spring Boot RESTful Microservice
    Microservices with Spring Boot
        Brief introduction to bootstrap.yml and application.yml
        A simple microservice example
            Creating a discovery service
            Creating a microservice (the Producer)
            Creating microservice consumers
                Load-balanced RestTemplate
    Brief introduction to Spring Data
        Apache Ignite repository
        Spring Data MongoDB
            Spring MongoDB data highlights
        Spring Data JPA
    小结

### 7. Creating API Gateway with Netflix Zuul Proxy
    The need for an API Gateway pattern
        Pros of the API Gateway pattern
        Cons of the API Gateway pattern
        API Gateway pattern components
    Implementing API Gateway using Netflix Zuul Proxy
        Including Zuul using Maven dependency
        Enabling the Zuul service proxy
        Configuring Zuul properties
        Adding Zuul filters
            Registering Zuul filters
    小结

### 8. Simplify HTTP API with Feign Client
    Declarative REST client&#xA0;&#x2013; Feign basics
    Including Feign in the cloud application
        Overriding Feign defaults
            Creating Feign clients
                Feign inheritance support
                Multiple interfaces
    Advanced usage of the Feign client
        Feign logging
    Exception handling
    Custom encoders and decoders
        Custom encoder
        Custom decoder
    Feign and Hystrix
    Unit testing Feign clients
    小结

### 9. Building Event-Driven and Asynchronous Reactive Systems
    Event-driven architecture patterns
        Mediator topology
        Broker topology
    Introduction to reactive programming
        Spring Reactive
        ReactiveX
    Introduction to Command Query Responsibility Segregation
        Introduction to the Event Sourcing pattern
        Introduction to Eventual consistency
    Building an event-driven Reactive Asynchronous System
    Introducing Spring Cloud Streaming
        Adding Kafka to your application
            Installing and running Kafka
            Configuration properties for Kafka
            Service used to write to Kafka
            Rest API controller
            Listening to a Kafka topic
    小结

### 10. Building Resilient Systems Using Hystrix and Turbine
    Circuit-breaker pattern
    Using the Hystrix library with a reference implementation
    Configuring Hystrix in your application
        Maven dependency
        Enabling circuit-breaker
        Adding the Hystrix annotation in services
            Error propagation
    Implementing a REST controller in customer service
    Building and testing customer service
    Customizing the default configuration
    Hystrix Metrics Stream
    Implementing Hystrix Dashboard in our project
    Turbine dashboard
        Turbine stream
    REST consumer with Hystrix and Feign
    小结

### 11. Testing Spring Boot Application
    Test-driven development
    Unit testing
        Advantages
        Disadvantages
        Other mock libraries
    Integration testing
        Benefits of testing with Spring
        Activating profiles for a test class
    JUnit tests for the Spring Boot application
    Using Mockito for mocking services
    Postman for testing RESTful service contracts
    小结

### 12. Containerizing Microservice
    Introducing containers to the microservice architecture
        Virtual machines versus containers
        Benefits of a container-oriented approach
        Drawbacks of a container-oriented approach
            Key concepts of the containers-oriented approach
    Getting started with Docker
        Installing Docker
        Installing Docker on Linux
        Installing Docker on Windows
            Docker commands
            Container-specific commands
        Docker architecture
        Docker Engine
        Docker container
        Writing Dockerfile
    Dockerizing any Spring Boot application
    Creating a Docker image using Maven
    Getting started with Docker Compose
        Installing Docker Compose
        Using Docker Compose
        Writing a docker-compose file
        Orchestration using a docker-compose file
        Scaling containers using docker-compose and load balancing
    Introducing Kubernetes
    小结

### 13. API Management
    API Management
        Advantages of using API Management software tools
        API Management tools
    Rate limiting
        Implementing rate limiting
    Learning about KONG
        Microservice REST APIs with the KONG architecture
        Using APIs without the KONG architecture
        Installing KONG
        Using the KONG API
            Features of the KONG API
    Swagger
        Usage of Swagger
        Using Swagger in a microservice
            Adding a Maven dependency
            Configuring Swagger 2 in your project
            Configuring Swagger UI in your project
            Customizing the Swagger UI meta-configuration
                Filtering an API from Swagger's documentation
            Customizing with Swagger annotations
        Advantages of Swagger
    小结

### 14. Deploying in Cloud (AWS)
    Spinning up an AWS EC2 instance
    Microservices architecture on AWS
        Publishing microservices to the Docker Hub
    Installing Docker on AWS EC2
    Running microservices on AWS EC2
    小结

### 15. Production Ready Service Monitoring and Best Practices
    Monitoring containers
    Logging challenges for the microservices architecture
    Centralized logging solution for the microservices architecture
        Log aggregation using the ELK stack
            Install Elasticsearch
            Install Logstash
            Install Kibana
        Requesting tracing using Sleuth
        Requesting tracing with Zipkin
            Adding the Zipkin server to your machine
    小结


©2019 http://docedit.cn/ WeChat ID: Grails1
