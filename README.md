Project showing stray output when built with gradle. This project just has H2, JPA and is auto
generated from start.spring.io no code or config changes have been made.  As you can see
from the output below gradlew is not capturing all the output.


```
 |master S:1 U:5 ✗| → ./gradlew build 
Starting a Gradle Daemon, 1 incompatible Daemon could not be reused, use --status for details

> Task :test
2020-03-04 10:03:39.248  INFO 41278 --- [extShutdownHook] o.s.s.concurrent.ThreadPoolTaskExecutor  : Shutting down ExecutorService 'applicationTaskExecutor'
2020-03-04 10:03:39.249  INFO 41278 --- [extShutdownHook] j.LocalContainerEntityManagerFactoryBean : Closing JPA EntityManagerFactory for persistence unit 'default'
2020-03-04 10:03:39.249  INFO 41278 --- [extShutdownHook] .SchemaDropperImpl$DelayedDropActionImpl : HHH000477: Starting delayed evictData of schema as part of SessionFactory shut-down'
2020-03-04 10:03:39.251  INFO 41278 --- [extShutdownHook] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Shutdown initiated...
2020-03-04 10:03:39.255  INFO 41278 --- [extShutdownHook] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Shutdown completed.

BUILD SUCCESSFUL in 29s
5 actionable tasks: 5 executed
```

Java version 11 being used.

```
 |master S:1 U:5 ✗| → java --version
openjdk 11.0.6 2020-01-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode)

```
