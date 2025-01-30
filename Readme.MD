# 🚀 Kafka with Docker Compose

This project sets up an **Apache Kafka** broker and **Zookeeper** using **Docker Compose**. Below are useful commands to manage Kafka topics and containers.

## 📦 Commands

### 🔹 Start the Containers (Detached Mode)
```sh
docker compose up -d

Stop the container 
docker compose down

To clean up unused docker objects
docker system prune -f

View logs
docker compose logs -f

Rebuild the container
docker compose up -d --build

list running containers
docker ps

Access the container shell
docker exec -it <container_name> bash

cd /opt/kafka/bin

To list kafka topics
./kafka-topics.sh --list --bootstrap-server localhost:9092 

Create a kafka topic
./kafka-topics.sh --create --topic test-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1

Describe a kafka topic
./kafka-topics.sh --describe --topic test-topic --bootstrap-server localhost:9092

Produce Messages to a Topic:
./kafka-console-producer.sh --topic test-topic --bootstrap-server
 localhost:9092

Consume Messages from a Topic:
./kafka-console-consumer.sh --topic test-topic --bootstrap-server localhost:9092 --from-beginning

```