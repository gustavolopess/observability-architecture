# Observability Architecture 👀🏛

Sample project to explore some observability concepts related with microservices architecture. Project for IF1007 (Microservices) class at Federal University of Pernambuco.

## Proposed Architecture

![proposed architecture](https://imgur.com/FqIrHNk.png "Agnostic Watcher architecture")

The idea is quite simple:

* There are some microservices (service 1, service 2, ..., service N) as shown at the image above
* Each microservice will have a [logstash](https://www.elastic.co/logstash) daemon sending logs to a centralized ElasticSearch cluster.
* Each microservice will have an endpoint designed to expose gauge and counter metrics to a centralized Prometheus
* A Grafana plugged to Prometheus is responsible to display dashboards based on ga uges and counter metrics
* The ElasticSearch cluster will have an alert system plugged in it. This alert system is described [here](https://github.com/gustavolopess/agnostic-watcher)

## Project Roadmap

The roadmap can be found on [this Trello board](https://trello.com/b/QKe5AeiW/roadmap-agnostic-watcher).