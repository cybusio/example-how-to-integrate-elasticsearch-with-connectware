# Cybus Learn - Elastic Stack

This repository describes how to integrate Elasticsearch with Cybus Connectware.

The purpose is to give Cybus Connectware users a guideline how to integrate
Connectware with Elasticsearch endpoints using a Filebeat with MQTT input.

## Prerequisites

The Cybus Connectware and an Elasticsearch Cluster endpoint are required.


## Integration Elasticsearch with Cybus Connectware

The test resources add complexity to the integration example stepwise
according to the corresponding Cybus Learn Article.

For a fast outcome get a free https://cloud.elastic.co demo instance
and note the CloudId and CloudAuth data in the service commissioning files

The different files have the following purpose:

- `elasticsearch-filebeat_0_initial`: initial filebeat with mqtt input
- `elasticsearch-filebeat_1_names`: fix names to identify service and context better in the search index
- `elasticsearch-filebeat_2_topics`: add data sources from simulators and continually send data

The simulators are extracted from the BAZ example in https://docs.cybus.io
and the [Cybus Learn Article "Service Basics"](https://learn.cybus.io/)


In order to test this just configure the two configuration parameters provided by the
elasticsearch cluster environment:

- `filebeatCloudId`
- `filebeatCloudAuth`

## Verify successful integration

To see a successful integration you may use Kibana in the Elastic Cloud console
and review the machine data continuously added to the search index.

## References

- [Elasticsearch](http://elastic.co/)
- [Filebeat Reference MQTT Input](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-mqtt.html)
- [Cybus Homepage](https://www.cybus.io/)
- [Cybus Connectware documentation](https://docs.cybus.io)
- [Cybus Learn Service Basics](https://learn.cybus.io/lessons/mqtt-basics/)
