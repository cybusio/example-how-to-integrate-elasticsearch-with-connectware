# How to integrate Elasticsearch with Connectware

This repository describes how to integrate Elasticsearch with Cybus Connectware.

The purpose is to give Cybus Connectware users a guideline how to integrate
Connectware with Elasticsearch endpoints using a Filebeat with MQTT input.

## Prerequisites

The Cybus Connectware and an Elasticsearch Cluster endpoints are required.

## Integration Elasticsearch with Cybus Connectware

The test resources add complexity to the integration example.

To achieve a quick outcome, obtain a free demo instance from https://cloud.elastic.co 
and write down the CloudId and CloudAuth data from the service commissioning files.

The different files have the following purpose:

- `elasticsearch-filebeat_0_initial`: initial filebeat with mqtt input
- `elasticsearch-filebeat_1_names`: fix names to identify service and context better in the search index
- `elasticsearch-filebeat_2_topics`: add data sources from simulators and continually send data

The simulators are extracted from the BAZ example in https://docs.cybus.io.

To test this, configure the following configuration parameters provided by the
elasticsearch cluster environment:

- `filebeatCloudId`
- `filebeatCloudAuth`

## Verify successful integration

To see a successful integration, you can use Kibana in the Elastic Cloud console
and review the machine data continuously added to the search index.

## References

- [Elasticsearch](http://elastic.co/)
- [Filebeat Reference MQTT Input](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-mqtt.html)
- [Cybus Homepage](https://www.cybus.io/)
- [Cybus Connectware documentation](https://docs.cybus.io)
