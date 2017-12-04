```
Docker build -t kafka-arm . 

Starting the container with `kafka-server-start.sh` and not passing in zookeeper environment variables will also start zookeeper 

`docker run -d -p 9092:9092 -p 2181:2181 -e KAFKA_HEAP_OPTS="-Xmx512m -Xms512m" -e KAFKA_ADVERTISED_HOST_NAME="<IP_OF_HOST_WITHOUT_PORT>" -e KAFKA_LISTENERS="PLAINTEXT://0.0.0.0:9092" isnit0/docker-kafka-arm  kafka-server-start.sh config/server.properties`

```
