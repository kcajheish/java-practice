running rabbitmq in container
```code
# latest RabbitMQ 3.13
docker run -it --rm --name rabbitmq -p 5672:5672 rabbitmq:3.13-management
```

install external dependencies for Marven project
```
rabbitmq
SLF4J API
SLF4J Simple
```

Then rabbitmq server will listen at port 5672. Once you send a message, you see logs like below:
```
2024-06-16 18:02:27 2024-06-16 10:02:27.066324+00:00 [info] <0.867.0> accepting AMQP connection <0.867.0> (192.168.65.1:18080 -> 172.17.0.2:5672)
2024-06-16 18:02:27 2024-06-16 10:02:27.125494+00:00 [info] <0.867.0> connection <0.867.0> (192.168.65.1:18080 -> 172.17.0.2:5672): user 'guest' authenticated and granted access to vhost '/'
2024-06-16 18:02:27 2024-06-16 10:02:27.163232+00:00 [info] <0.867.0> closing AMQP connection <0.867.0> (192.168.65.1:18080 -> 172.17.0.2:5672, vhost: '/', user: 'guest')
```
