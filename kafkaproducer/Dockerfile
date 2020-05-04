FROM openjdk:8
COPY . /tmp
WORKDIR /tmp
LABEL "com.datadoghq.ad.logs"='[{"source": "java", "service": "KafkaProducer"}]'
ENTRYPOINT ["java","-javaagent:dd-java-agent.jar","-Ddd.agent.host=localhost","-Ddd.jmxfetch.statsd.host=localhost","-Ddd.trace.global.tags=env:kafka","-Ddd.agent.port=8126","-Ddd.service.name=KafkaProducer","-Ddd.logs.injection=true","-Ddd.trace.analytics.enabled=true","-Ddd.kafka.analytics.enabled=true","-Ddd.servlet.analytics.enabled=true","-Ddd.spring-web.analytics.enabled=true","-jar","target/KafkaConsumer-0.0.1-SNAPSHOT.jar"]
