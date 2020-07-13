# Kafka Docker

## Kafka tools & Monitoring
- Kafka Docker : https://github.com/wurstmeister/kafka-docker
- https://github.com/simplesteph/kafka-stack-docker-compose
- Kafka Docker Listeners : https://rmoff.net/2018/08/02/kafka-listeners-explained/
- Kafka Docker Listeners : https://stackoverflow.com/questions/48731030/no-security-protocol-defined-for-listener-plaintext-tcp
- https://torres.atlassian.net/wiki/spaces/TDD/pages/621674615/Kafka+ops+Management+Monitoring
- https://github.com/freepsw/kafka-monitoring


### (tools) kafka - cli
- wget https://archive.apache.org/dist/kafka/2.0.1/kafka_2.12-2.0.1.tgz

### (tools) kafka Conduktor
- https://www.conduktor.io/

### kafka manager (CMAK)
- https://github.com/hleb-albau/kafka-manager-docker (CMAK)
- kafka manager : http://localhost:9000/

### zookeeper Navigator
- https://github.com/elkozmon/zoonavigator

### kafka REST Proxy (confluent) & UI
- https://docs.confluent.io/current/kafka-rest/index.html
- https://github.com/lensesio/kafka-topics-ui

### kafka Connect (confluent) & UI
- https://docs.confluent.io/current/connect/index.html
- https://github.com/lensesio/kafka-connect-ui

### kafka schema registry (confluent) & UI
- https://docs.confluent.io/current/schema-registry/index.html
- https://github.com/lensesio/schema-registry-ui

### Prometheus - Kafka Exporter
- https://github.com/danielqsj/kafka_exporter
- https://medium.com/@agrajm/monitoring-kafka-on-kubernetes-with-prometheus-5b1d1518102
- https://grafana.com/grafana/dashboards/7589

### Prometheus - JMX Exporter
- https://github.com/prometheus/jmx_exporter
- https://github.com/Mousavi310/kafka-grafana
- https://medium.com/@mousavi310/monitor-apache-kafka-using-grafana-and-prometheus-873c7a0005e2


---

### kafka - cli

```
wget https://archive.apache.org/dist/kafka/2.0.1/kafka_2.12-2.0.1.tgz
tar -xvf kafka_2.12-2.0.1.tgz

bin/kafka-console-producer.sh --broker-list localhost:9092 --topic project-topic01
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic project-topic01 --from-beginning --timeout-ms 3000 --max-messages 2

bin/kafka-topics.sh --zookeeper localhost:2181 --list
bin/kafka-topics.sh --zookeeper localhost:2181 --topic project-topic01 --create --partitions 1 --replication-factor 1 --if-not-exists

bin/kafka-topics.sh --zookeeper localhost:2181 --topic project-topic01 --describe
bin/kafka-topics.sh --zookeeper localhost:2181 --topic project-topic01 --delete
```