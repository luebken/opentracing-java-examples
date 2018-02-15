# OpenTracing Java Examples

This repository contains various example apps instrumented with OpenTracing API and framework integrations.

## Start tracing with Jaeger

```bash
docker run -p6831:6831/udp -p6832:6832/udp \
  -p5778:5778 -p16686:16686 -p14268:14268 jaegertracing/all-in-one:latest
```
open http://localhost:16686 for the Jaeger UI

## Spring Boot
[Video](https://youtu.be/RvCcWltMY7U)

```bash
cd spring-boot
./mvnw clean install
java -jar target/demo-opentracing-0.0.1-SNAPSHOT.jar
# test:
curl http://localhost:8080/chaining
```

Tracing is done automatically via https://github.com/opentracing-contrib/java-spring-web#how-does-the-server-tracing-work

## JAX-RS (Wilfly Swarm)
[Video](https://youtu.be/gVwLenPH8SY)

```bash
mvn wildfly-swarm:run
```
