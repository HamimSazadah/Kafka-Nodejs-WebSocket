# Kafka-Nodejs-WebSocket
source : https://medium.com/@stressed83/live-streaming-data-using-kafka-node-js-websocket-and-chart-js-8750acad549c


# run zookeper server
bin\windows\zookeeper-server-start.bat config\zookeeper.properties

# run kafka server
bin\windows\kafka-server-start.bat config\server.properties

# create topic
bin\windows\kafka-topics.bat --create --topic webSocket --bootstrap-server localhost:9092

# check topic
bin\windows\kafka-topics.bat --describe --topic webSocket --bootstrap-server localhost:9092

# write event to topic
bin\windows\kafka-console-producer.bat --topic webSocket --bootstrap-server localhost:9092

# read topic
bin\windows\kafka-console-consumer.bat --topic webSocket --from-beginning --bootstrap-server localhost:9092

![alt](https://github.com/HamimSazadah/Kafka-Nodejs-WebSocket/blob/master/ss.jpg)
