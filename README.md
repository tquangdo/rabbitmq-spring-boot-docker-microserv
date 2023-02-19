# rabbitmq-spring-boot-docker-microserv 🐳

![Stars](https://img.shields.io/github/stars/tquangdo/rabbitmq-spring-boot-docker-microserv?color=f05340)
![Issues](https://img.shields.io/github/issues/tquangdo/rabbitmq-spring-boot-docker-microserv?color=f05340)
![Forks](https://img.shields.io/github/forks/tquangdo/rabbitmq-spring-boot-docker-microserv?color=f05340)
[![Report an issue](https://img.shields.io/badge/Support-Issues-green)](https://github.com/tquangdo/rabbitmq-spring-boot-docker-microserv/issues/new)

## reference
[youtube](https://www.youtube.com/watch?v=DvZVFQFjzsQ)

## version
```shell
java -version
# openjdk version "17.0.2" 2022-01-18
# OpenJDK Runtime Environment Temurin-17.0.2+8 (build 17.0.2+8)
mvn -version
# Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
# Maven home: /opt/homebrew/Cellar/maven/3.8.5/libexec
```
- need to map with `sender/Dockerfile` & `receiver/Dockerfile`
```bash
FROM maven:3.8.3-openjdk-17
```

## create project
- create spring boot project: `sender` & `receiver`
![mvn](screenshots/mvn.png)

## src code
1. ### Receiver.java
    - refer [Create a RabbitMQ Message Receiver](https://spring.io/guides/gs/messaging-rabbitmq/)
1. ### ReceiverApplication.java
    - refer [Register the Listener and Send a Message](https://spring.io/guides/gs/messaging-rabbitmq/)
1. ### Sender.java
    - refer [Send a Test Message](https://spring.io/guides/gs/messaging-rabbitmq/)

## demo
```shell
docker-compose up --build
```
- will see `create new connection rabbitMQ...`
![mq](screenshots/mq.png)
- access `localhost:8080` will see default page of spring boot
- access `localhost:8080/dotq deptrai dfgsdgsdfgdgf 123` will see `receiver    | Received <dotq deptrai dfgsdgsdfgdgf 123>` in terminal and in browser will be:
![demo](screenshots/demo.png)
