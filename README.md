# TestKafkaApplication

1. Run Kafka and Zookeeper images from Docker:

`docker-compose up -d`

2. Run TestKafkaApplication

`Press green triangle in your IDE ;-)`

3. Send message:

`curl -X POST -H "Content-Type: text/plain" -d "Hello Kafka" http://localhost:8080/send`

4. See list of topics:

`docker exec -it kafka kafka-topics --list --bootstrap-server localhost:9092`

5. See list of messages for chosen topic:

`docker exec -it kafka kafka-console-consumer \
   --bootstrap-server localhost:9092 \
   --topic test-topic \
   --from-beginning`