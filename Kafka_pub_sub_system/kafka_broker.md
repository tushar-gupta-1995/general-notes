# Kafka Cluster Brain
Within a kafka cluster, a control plane can be considered a brain. It handles: 
- Controller: The controller is a designated node responsible for managing the state of the entire Kafka cluster. It handles tasks such as leader election for partitions, monitoring the health of brokers, and triggering reassignments when brokers join or leave the cluster.

- Topic Management: The control plane handles the creation, deletion, and configuration of topics. It keeps track of the metadata, such as the number of partitions and their distribution across brokers.

- Broker Coordination: The control plane assists in the discovery and registration of brokers in the cluster. It keeps track of the live brokers and their capabilities.

- Partition Reassignment: When brokers are added or removed from the cluster, the control plane is responsible for reassigning partitions to maintain data replication and balance the load.

# kafka topic
a kafka topic is a stream of data, analogous to sql server table, but remember a topis is just a log.
## Log data strcuture properties
- immutable
- time identifier attached
- have offset to determine the position
- append only 

Kafka replicates these logs(topics) across multiple brokers (but there is only one leader/primary broker per partition)
kafka topics are written as logs of raw data+metadata(like offset)
This way a consumer can seek a particular offset to replay messages.

## kafka message
a kafka message is a key value pair.
IF a message does not provide a key, the messages are stored in round robin way in partition.
BUT if it has a key, the message goes into a partition determined by the key,(maybe the key is hashed to determine the partition)
This guarantees that message with the same key goes into the same partition.
### Risk
This also creates a risk, if a particular key repeats too much, one parition will become abnormally large..then others


# kafka partition
Kafka partitions a single topic and stores them on different nodes in a cluster for easier management.
This a single consumer can connect to multiple brokers parallely for faster processing.
Kafka elects a leader broker, for each partition.

# kafka broker
consider broker as a storage node in kafka.