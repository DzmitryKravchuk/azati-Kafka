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

To stop all services and clear docker call:

```
docker-compose stop \
docker-compose rm -f
```
###Additionally listing of metriks from Jmeter test execution:

1,000 REQUESTS (100 threads created in 1 sec. with 10 loop):
```
summary =   1000 in 00:00:03 =  319.3/s Avg:   212 Min:    31 Max:   582 Err:     0 (0.00%)
```

100,000 REQUESTS (1000 threads created in 10 sec. with 100 loop):
```
summary = 100000 in 00:02:24 =  696.2/s Avg:  1322 Min:     3 Max:  8095 Err:     0 (0.00%)
```

1 million REQUESTS (1000 threads created in 10 sec. with 1000 loop):
```
summary = 1000000 in 00:21:50 =  763.6/s Avg:  1295 Min:     3 Max: 15677 Err:     0 (0.00%)
```
