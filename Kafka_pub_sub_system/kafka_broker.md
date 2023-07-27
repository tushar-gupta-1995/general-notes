# Kafka Cluster Brain
Within a kafka cluster, a control plane can be considered a brain. It handles: 
- Controller: The controller is a designated node responsible for managing the state of the entire Kafka cluster. It handles tasks such as leader election for partitions, monitoring the health of brokers, and triggering reassignments when brokers join or leave the cluster.

- Topic Management: The control plane handles the creation, deletion, and configuration of topics. It keeps track of the metadata, such as the number of partitions and their distribution across brokers.

- Broker Coordination: The control plane assists in the discovery and registration of brokers in the cluster. It keeps track of the live brokers and their capabilities.

- Partition Reassignment: When brokers are added or removed from the cluster, the control plane is responsible for reassigning partitions to maintain data replication and balance the load.

# kafka topic
a kafka topic is a stream of data, analogous to sql server table.
kafka topics are written as logs of raw data+metadata(like offset)
This way a consumer can seek a particular offset to replay messages.

# kafka partition
Kafka partitions a single topic and stores them on different nodes in a cluster for easier management.
This a single consumer can connect to multiple brokers parallely for faster processing.
Kafka elects a leader broker, for each partition.