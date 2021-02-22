# KafkaAsDatabase
Kafka as a database - Online Event Processing (OLEP). A simple implementation of the idea mentioned https://www.youtube.com/watch?v=BuE6JvQE_CY&list=WL&index=2&t=30s

# Use Case
* Strong consistency with series of event to achieve something similar with OLTP transaction through commit, but potentially in distributed and much more scalable way.
* Decoupled web service of a update


# Example - Bank Account Transaction
1. User trigger a request
2. A "Withdraw" request send to a Kafka Topic
3. A "Update" request send to another Kafka topic
4. 3 Consumers consumes the "Update" topic, index, cache and DB tables
5. Archieve consistency result even if crash, as log can be recovered from where it fails.


# Example - Bank Account Transaction (Strong Consistency)
