azati-Kafka
===

`producer` is a simple REST application for saving a number to Apache Kafka topic
`consumer` reads the message from Kafka topic and saves the number to DB
 
Go to producer and consumer directory and build each of them first:

```
gradle build
```

From the root project to run all services (including Zookeeper, Kafka, DB) simply call:

```
docker-compose up
```

###For manual testing you can use this end-point:

- POST to URL:  http://localhost:8081/message/publish

set any number to `intValue` parameter in request body
```
{ "intValue": 10 }
```
To stop all services and clear docker call:

```
docker-compose stop \
docker-compose rm -f
```