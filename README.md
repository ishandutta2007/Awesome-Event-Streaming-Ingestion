# Awesome-Event-Streaming-Ingestion

# Top Event Streaming & Ingestion Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on High-Throughput Event Ingestion, Message Brokers & Self-Hosted Streaming Infrastructure*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Event Streaming & Ingestion**. These tools enable applications and organizations to ingest, route, buffer, and process high-volume event streams in real time—powering data pipelines, microservices communication, IoT telemetry, and AI system backends.

**Examples** include Confluent Cloud, Amazon MSK, Redpanda Cloud, Azure Event Hubs, Google Cloud Pub/Sub, IBM MQ, Solace PubSub+, CloudKarafka, and HiveMQ (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, protocol flexibility, and transparent event infrastructure—ideal for teams that need data sovereignty, avoid per-message SaaS fees, and require auditable streaming pipelines. The open-source landscape is anchored by **Apache Kafka** (the distributed log standard), **Redpanda** (Kafka-compatible without JVM/ZooKeeper), **Apache Pulsar** (multi-tenant pub-sub), and **RabbitMQ** (mature message broker), with specialized options like **HiveMQ** and **Mosquitto** for MQTT/IoT ingestion, and emerging projects like **Busbar** for AI-specific routing.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Confluent Cloud](https://www.confluent.io/confluent-cloud/)**  
  Fully managed Kafka service from the company founded by Kafka's creators. Offers Schema Registry, ksqlDB, and Connectors as managed add-ons. The reference platform for teams that want Kafka without operational burden.

- **[Amazon MSK](https://aws.amazon.com/msk/)**  
  AWS's managed Kafka service with IAM, mTLS, and SASL/SCRAM authentication. Integrates with CloudWatch for metrics and S3/CloudWatch/Firehose for log delivery. Best for AWS-native architectures requiring managed Kafka.

- **[Redpanda Cloud](https://redpanda.com/cloud)**  
  Kafka-compatible streaming platform with Serverless, Dedicated, and BYOC deployment options. Serverless tier bills by ingress, egress, partitions, and retained data. Kafka API compatible, so existing clients work without code changes.

- **[Azure Event Hubs](https://azure.microsoft.com/en-us/products/event-hubs/)**  
  Azure's native event streaming platform with built-in Apache Kafka compatibility. Standard tier supports 1MB max event size and 7-day retention; Premium extends to 90-day retention and 100 consumer groups. Best for Azure-native workloads wanting Kafka compatibility.

- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**  
  Google's globally distributed messaging service. Not natively Kafka-compatible—migration requires client changes. Supports message ordering via ordering keys, dead-letter topics, and up to 31 days retention. Best for GCP-native architectures that don't require Kafka protocol.

- **[IBM MQ](https://www.ibm.com/products/mq)**  
  Enterprise messaging middleware with deep mainframe and IBM ecosystem integration. Reliable, secure, and scalable for mission-critical integration. Proprietary and typically enterprise-priced.

- **[Solace PubSub+](https://solace.com/)**  
  Event streaming and management platform supporting multiple protocols (AMQP, MQTT, JMS, REST) with a unified broker. Strong for hybrid cloud and IoT use cases.

- **[CloudKarafka](https://www.cloudkarafka.com/)**  
  Hosted Apache Kafka service with plans from $49/month (Developer) to $499 (Business). 99.95% SLA on dedicated plans. Note: CloudKarafka was discontinued; verify availability before committing .

- **[HiveMQ Cloud](https://www.hivemq.com/)**  
  Managed MQTT broker for IoT and event-driven architectures. The open-source HiveMQ Community Edition can be self-hosted; the cloud tier adds managed infrastructure and enterprise features .

## Open-Source GitHub Projects

- **[Apache Kafka](https://github.com/apache/kafka)**  
  The distributed event streaming platform standard. High-throughput, fault-tolerant, durable log storage. Requires JVM and (historically) ZooKeeper, though KRaft mode eliminates ZooKeeper in newer versions. Apache 2.0 licensed with 31k+ stars . Best for organizations that need the full Kafka ecosystem and can manage operational complexity.

- **[Redpanda](https://github.com/redpanda-data/redpanda)**  
  Kafka API-compatible streaming platform built in C++ with no JVM or ZooKeeper. Claims up to 10x performance improvement over Apache Kafka with simpler operations. Source-available under BSL with a free Community Edition . Best for teams that want Kafka compatibility without Kafka's operational overhead.

- **[Apache Pulsar](https://github.com/apache/pulsar)**  
  Distributed pub-sub messaging system with multi-tenancy, tiered storage, and strong durability guarantees. Apache 2.0 licensed with 13,950+ stars . Best for organizations that need multi-tenant event streaming with geo-replication.

- **[RabbitMQ](https://github.com/rabbitmq/rabbitmq-server)**  
  Mature, widely-deployed open-source message broker supporting AMQP, MQTT, and STOMP. Flexible routing via exchanges and queues. Best for traditional message queue workloads and microservices communication requiring complex routing logic.

- **[Apache RocketMQ](https://github.com/apache/rocketmq)**  
  Cloud-native messaging and streaming platform with low latency and high throughput. Java-based, Apache 2.0 licensed. Popular in Chinese enterprise environments . Best for teams that need a Kafka alternative with different tradeoffs.

- **[Apache ActiveMQ](https://github.com/apache/activemq)**  
  High-performance multi-protocol message broker supporting JMS, AMQP, MQTT, and STOMP. Apache 2.0 licensed, Apache top-level project . Best for JMS-centric enterprise environments and legacy Java integration.

- **[HiveMQ Community Edition](https://github.com/hivemq/hivemq-community-edition)**  
  Open-source MQTT broker for IoT and event-driven architectures. Java-based with a plugin system. The Community Edition is free; enterprise extensions add clustering and advanced security . Best for IoT ingestion pipelines requiring MQTT protocol support.

- **[Eclipse Mosquitto](https://github.com/eclipse/mosquitto)**  
  Lightweight open-source MQTT broker written in C. Fully supports MQTT 3.1 and 3.1.1. Small footprint makes it suitable for constrained devices and edge deployments . Best for resource-constrained IoT gateways.

- **[Eclipse Zenoh](https://github.com/eclipse-zenoh/zenoh)**  
  Next-generation pub-sub/overlay protocol with native bridges to MQTT, Kafka, and WebSocket. Dual-licensed EPL-2.0/Apache-2.0 with 2.8k+ stars . Best for robotic, edge, and WAN-spanning deployments where traditional brokers become bottlenecks.

- **[Busbar](https://github.com/GetBusbar/busbar)**  
  Single-binary AI control plane that routes and fails over requests across AI providers (Anthropic, OpenAI, Gemini, Cohere, Bedrock). Apache 2.0 licensed, ~5MB Docker image. Provides one endpoint for chat, embeddings, images, and audio with budget enforcement and observability . **Note**: While positioned for AI routing rather than general event streaming, it's an emerging option for AI-specific ingestion and failover.

### Additional Strong Open-Source Options

- **ZeroMQ** — High-performance asynchronous messaging library rather than a broker. Best for low-latency, broker-less messaging within applications .
- **Apache Qpid** — AMQP-compliant messaging tools with multi-language support. Best for AMQP-centric enterprise integration .
- **VerneMQ** — Distributed MQTT broker in Erlang, scales horizontally for high connection counts. Best for large-scale IoT deployments .
- **Frameworks for building custom systems**: Pair **Apache Kafka** or **Redpanda** as the durable event backbone with **HiveMQ** or **Mosquitto** for IoT MQTT ingestion, and **Busbar** for AI provider routing. Use **RabbitMQ** for complex routing logic and **Pulsar** when multi-tenancy is required.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Event streaming platforms vary significantly in throughput characteristics, operational complexity, and protocol support; benchmark against your workload before committing.
- Self-hosted streaming infrastructure requires proper cluster sizing, replication configuration, monitoring, and disaster recovery planning.
- CloudKarafka appears to have discontinued service; verify current availability before selecting it .

---

**Made for data engineers, platform teams, IoT architects, and developers building real-time event-driven systems.**  
Let's make event streaming and ingestion more open, compatible, and accessible.
