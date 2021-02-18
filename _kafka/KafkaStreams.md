# Kafka Streams

Kafka Streams is a ***client library*** for processing and analyzing data stored in Kafka.

* It is an artifact that can be easily embedded in any Java application.
  
* Apache Kafka is the only external dependency.

* Fault-tolerant local state.

* Exactly-once processing semantics even when there is a failure on either Streams clients or Kafka brokers in the moddle of processing.

* High-level streams DSL and low-level Processor API.

## Concepts

### Streams

A stream is an ordered, replayable, and fault-tolerant sequence of immutable data records, where a data record is defined as a key-value pair.

### Stream Processing Application

### Stream Processor

#### Source Processor

#### Sink Processor

> Normal processor nodes, other remote systems can also be accessed while proceesing the current record there by, the processed results can always be written to an external system.

### Time

#### Event Time

#### Processing Time

#### Ingestion Time

#### Stream Time

### Table

### Aggregations

### Windowing

## Stream-Table Duality

## Processing Guarantees

Note the key difference between Kafka Streams end-to-end exactly-once guarantee with other stream processing frameworks' claimed guarantees is that Kafka Streams tightly integrates with the underlying Kafka storage system and ensure that commits on the input topic offsets, updates on the state stores, and writes to the output topics will be completed atomically instead of treating Kafka as an external system that may have side-effects.
