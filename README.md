# OpenTracing Java Examples

This repository contains various example apps instrumented with OpenTracing API and framework integrations.

## Start tracing system
Choose tracing system, note that some code changes might be required, depending on which tracer is initialized.

```bash
docker run --rm -it --network=host jaegertracing/all-in-one
docker run --rm -it -p 9411:9411 openzipkin/zipkin
```

## Spring boot
```bash
mvnw clean install
java -jar target/demo-opentracing-0.0.1-SNAPSHOT.jar
```