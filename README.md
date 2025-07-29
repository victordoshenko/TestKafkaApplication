# Test Kafka Application

1. Download Kafka and Zookeeper images from Docker Hub (version 7.3.13) using your Docker Desktop:
![Снимок экрана 2025-07-29 в 14 36 49](https://github.com/user-attachments/assets/47b0648b-c684-4af1-96c2-94708e03f0ad)

2. Run Kafka and Zookeeper images from Docker:

`docker-compose up -d`
![6E2878B3-4DEC-4D3B-9987-64ED4B9E7E9D_1_201_a](https://github.com/user-attachments/assets/2c3786c3-6d56-44d3-8f7f-0991c4806f92)

3. Run TestKafkaApplication

`Press green triangle in your IDE ;-)`
![95CC4784-A66E-4B5A-BEAD-53B612B560DE_1_201_a](https://github.com/user-attachments/assets/251fc375-4c0c-4c60-b53a-b38623c03162)

4. Send message:

`curl -X POST -H "Content-Type: text/plain" -d "Hello Kafka" http://localhost:8080/send`
![7928D3AF-29EB-472C-8F92-639BA6515CB1_1_201_a](https://github.com/user-attachments/assets/5e552464-94fc-4108-bf8d-c814b66a6ccc)

5. See list of topics:

`docker exec -it kafka kafka-topics --list --bootstrap-server localhost:9092`

6. See list of messages for chosen topic:

`docker exec -it kafka kafka-console-consumer \
   --bootstrap-server localhost:9092 \
   --topic test-topic \
   --from-beginning`
