# Spring

* Spring 启动时设置参数

Spring 启动时可设置参数，如修改配置文件`application.properties`的路`--spring.config.location=/confg`，但需要注意的是`SpringApplication.run(App.class, args)`，**必须**包括`args`，否者启动参数将无效。

* `@AutoConfigureTestDatabase`

自动配置一个内存数据库用在测试，需要在Maven 的配置文件中引入内存数据库，如`H2db`。

* `@DirtiesContext`

在测试中可清理测试缓存，如清理内存数据库中的表，清理单例模式的类，使其回到初始状态。

* `Spring boot dependencies`

在maven配置文件中如下引入`Spring boot`的依赖
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-dependencies</artifactId>
    <version>${spring.boot.version}</version>
    <type>pom</type>
    <scope>import</scope>
</dependency>
```

子模块可以引入父模块的依赖包而不需要`spring-boot-starter-parent`。



