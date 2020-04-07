# kafka-quickstart
Deploy Kafka environment and Datadog agent


# Uncompress file

tar -xvf My-kafka-test.tgz

# Update docker-compose.yaml with API Key

```
 datadog-agent:
    network_mode: host
    image: datadog/agent:latest-jmx
    container_name: datadog-agent
    environment:
     - DD_PROCESS_AGENT_ENABLED=true
     - DD_API_KEY=xxx
```

# Start cluster
docker-compose up

# Create message
## Connect to kafka producer
`docker exec -it kafkaproducer /bin/bash``
`/tmp/send_1000_messages``
 


