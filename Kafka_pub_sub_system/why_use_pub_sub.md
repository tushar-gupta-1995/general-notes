# Older Ideas : Push And Poll
- Imagine having a microservice environment of 8 microservices, where 5 microservices create a metric_server which continuously `push` the metric data to a server exposed by microservice 6 in its local environment.
- The 6th microservice is aggregating and partitioning and storing all the metrics and exposes an api that can be used to `get` metric data.
- Microservice 7 and 8 are querying the server exposed by microservice 6 and using it for their own purposes,

## Problem
- In the above scenario microservice 6 can easily be overwhelmed by the amount of metrics pushed to it.
- microservice 6 has an additional overhead of partitioning and aggregating data.
- microservice 6 has an additional overhead of serving microservice 7 and 8.
- microservice 6 needs an additional overhead of data replication if it needs reliability
- microservice 6 can easily become a bottleneck.

# Possible Solution?
What if we create 5 message queues, one for each microservice, imagine them as streams, but instead of water, metric is flowing through them.
microservice 7 and 8 can just subscribe to the queues they are interested in, and metrics will be available to them for consumption.
We would still NEED to ACCOUNT for if microservice 7 or 8 suddenly experience a `network` issue or `choke` and thus might lose data.
We would need to provide a schema to the microservice 7 and 8 so they know the fields and their datatypes and deserialise them.
We would also need a way to scale the data being sent in the queues.
`Kafka` solves a lot of these.