### Basic commands kafka
#### we are running kafka instance in docker container, so below commands are for docker env.
- how to list topics in kafka
  ```bash
  docker exec -it kafka kafka-topics --bootstrap-server kafka:9092 --list
  ```
- create topic
    ```bash
    docker exec -it kafka kafka-topics --bootstrap-server kafka:9092 --create --topic test-topic --partitions 1 --replication-factor 1
    ```
- describe topic
    ```bash
    docker exec -it kafka kafka-topics --bootstrap-server kafka:9092 --describe --topic test-topic
    ```
- produce message to topic
    ```bash
    docker exec -it kafka kafka-console-producer --bootstrap-server kafka:9092 --topic test-topic
    ```
- consume messsage from topic
    ```bash
    docker exec -it kafka kafka-console-consumer --bootstrap-server kafka:9092 --topic test-topic --from-beginning
    ```
- delete topic
    ```bash
    docker exec -it kafka kafka-topics --bootstrap-server kafka:9092 --delete --topic test-topic-1
    ```

---