########################
SLF4J
########################

Java 中比较常用的日志框架：

#. log4j(Log for Java)：Apache 的一个开源项目，七种日志级别：OFF、FATAL、ERROR、WARN、INFO、DEBUG、TRACE
#. logback：是一个很成熟的日志框架，其实 logBack 和 log4j 出自一个人之手，这个人就是 Ceki Gülcü。logback 比 log4j 大约快 10 倍、消耗更少的内存，迁移成本也很低，自动压缩日志、支持多样化配置、不需要重启就可以恢复 I/O 异常等优势
#. log4j2：log4j2已经不仅仅是 log4j 的一个升级版本了，而是从头到尾被重写的，这可以认为这其实就是完全不同的两个框架

Spring Boot 默认使用 logback，但相比较而言，log4j2 在性能上面会更好。SpringBoot 高版本都不再支持 log4j，而是支持 log4j2。log4j2，在使用方面与 log4j 基本上没什么区别，比较大的区别是 log4j2 不再支持 properties 配置文件，支持 xml、json 格式的文件。

《阿里巴巴Java开发手册》，其中有一条规范做了「强制」要求：

    应用中不可直接使用日志系统（Log4j Logback）中的 API，而应依赖使用日志框架 SLF4J 中的 API，使用日志门面模式的日志框架，有利于维护和各个类的日志处理方式统一。

SLF4J
============
Java 简易日志门面（Simple Logging Facade for Java，缩写 SLF4J），它并不是真正的日志框架,他是对所有日志框架制定的一种规范、标准、接口，并不是一个框架的具体的实现，因为接口并不能独立使用，需要和具体的日志框架实现配合使用。可以在软件部署的时候决定要使用的 Logging 框架，目前主要支援的有 Java logging API、log4j 及 logback 等框架。

接口用于定制规范，可以有多个实现，使用时是面向接口的(导入的包都是 slf4j 的包而不是具体某个日志框架中的包)，即直接和接口交互，不直接使用实现，所以可以任意的更换实现而不用更改代码中的日志相关代码。


slf4j+logback
=================
Spring boot默认支持的就是slf4j+logback的日志框架，想要灵活的定制日志策略，只需要我们在src/main/resources下添加配置文件即可，只是默认情况下配置文件的命名需要符合以下规则：

* logback.xml
* logback-spring.xml

其中logback-spring.xml是官方推荐的，并且只有使用这种命名规则，才可以配置不同环境使用不同的日志策略这一功能。




log4j2 依赖
========================
.. code-block:: XML
    :linenos:

    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <!-- 去掉logback配置 -->
            <exclusions>
                <exclusion>
                    <groupId>org.springframework.boot</groupId>
                    <artifactId>spring-boot-starter-logging</artifactId>
                </exclusion>
            </exclusions>
        </dependency>

        <!-- 引入log4j2依赖 -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-log4j2</artifactId>
        </dependency>
    </dependencies>



slf4j使用
========================

.. code-block:: XML
    :linenos:

    import org.slf4j.Logger;
    import org.slf4j.LoggerFactory;

    // 这了两种写法都 OK，推荐第一种，不用每次都要修改类名
    private static final Logger logger = LoggerFactory.getLogger(this.getClass());
    private static final Logger logger = LogManager.getLogger(UserController.class);
    //...
    logger.debug("this is debug");
    logger.info("this is info");