# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **learning/study repository** for Apache Kafka - a collection of educational documentation covering Kafka concepts, installation, and usage. It is not the Apache Kafka source code.

## Repository Structure

- `01_kafka_installation_ubuntu.txt` - Kafka 3.9.0 KRaft mode installation on Ubuntu
- `02_kafka_fundamentals.txt` - Introduction to Kafka architecture and use cases
- `03_kafka_core_concepts.txt` - Topics, Partitions, Offsets, Segments, Replication
- `04_kafka_performance.txt` - Disk storage, sequential I/O, zero-copy, batching
- `05_kafka_producers.txt` - Producer configuration, partitioning, idempotence
- `06_kafka_consumers.txt` - Consumer groups, offsets, poll loop, patterns
- `07_kafka_rebalancing.txt` - Rebalance protocols, assignment strategies, static membership
- `08_kafka_lag.txt` - Consumer lag monitoring, causes, alerting, remediation
- `09_kafka_rate_limiting.txt` - Quotas, throttling, multi-tenant scenarios
- `10_kafka_connect.txt` - Source/sink connectors, transforms, REST API
- `11_kafka_streams.txt` - KStream, KTable, topology, windowing, state stores
- `kafka_commands.txt` - CLI commands reference (topics, producers, consumers, offsets)
- `kafka_streams_commands.txt` - Kafka Streams CLI (reset, internal topics, state stores)
- `NextTopics` - Learning roadmap and progress tracker

## Kafka Environment (as documented)

**Installation Path:** `/opt/kafka`
**Bootstrap Server:** `localhost:9092`
**Mode:** KRaft (Zookeeper-free)
**Config:** `/opt/kafka/config/kraft/server.properties`

## Common Kafka CLI Commands

```bash
# Start/Stop Kafka
kafka-start                                    # alias for daemon start
kafka-stop                                     # stop server

# Topics
kafka-topics.sh --list --bootstrap-server localhost:9092
kafka-topics.sh --create --topic <name> --bootstrap-server localhost:9092 --partitions 3 --replication-factor 1
kafka-topics.sh --describe --topic <name> --bootstrap-server localhost:9092

# Producer
kafka-console-producer.sh --topic <name> --bootstrap-server localhost:9092

# Consumer
kafka-console-consumer.sh --topic <name> --bootstrap-server localhost:9092 --from-beginning

# Consumer Groups
kafka-consumer-groups.sh --list --bootstrap-server localhost:9092
kafka-consumer-groups.sh --describe --group <name> --bootstrap-server localhost:9092
```

## Learning Progress

Completed: Installation, Fundamentals, Core Concepts, Performance, Producers, Consumers, Rebalancing, Consumer Lag, Rate Limiting, Kafka Connect, Kafka Streams
Pending: Spring Boot
