%md
# Commnads

## Download and extract kafka
- --wget https://archive.apache.org/dist/kafka/2.8.0/kafka_2.12-2.8.0.tgz
- --tar -xzf kafka_2.12-2.8.0.tgz
  
## start ZooKeeper
- --cd kafka_2.12-2.8.0
- --bin/zookeeper-server-start.sh config/zookeeper.properties

## Start the Kafka broker service
- --cd kafka_2.12-2.8.0
- --bin/kafka-server-start.sh config/server.properties

## Create a topic
- --cd kafka_2.12-2.8.0
- --bin/kafka-topics.sh --create --topic <topic-name> --bootstrap-server localhost:9092

## Start Producer
- --bin/kafka-console-producer.sh --topic <topic-name> --bootstrap-server localhost:9092
- -- wait for '>'
- -- > "message"

## Start Consumer
- --cd kafka_2.12-2.8.0
- --bin/kafka-console-consumer.sh --topic <topic-name> --from-beginning --bootstrap-server localhost:9092

## Explore Kafka directories.
- --Kafka uses the directory /tmp/kakfa-logs to store the messages.
- --Explore the folder news-0 inside /tmp/kakfa-logs.
- --This is where all the messages are stored.
- --Explore the folder /home/project/kafka_2.12-2.8.0
- --This folder has the below 3 sub directories.
