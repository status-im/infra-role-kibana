# Description

This role configures [Kibana](https://www.elastic.co/guide/en/kibana/7.5/index.html) Dashboard which is part of the [ELK Stack](https://www.elastic.co/elk-stack) which facilitates aggregation, collection, and querying of vast amounts of logs from multiple hosts and services.

# Usage

The dashboard is available at https://kibana.status.im/ and is hosted on a single host currently. It makes use of an ElasticSearch load balancer configured by the [`elasticsearch-lb`](../elasticsearch-lb/README.md) role which connects to the ES cluster and queries it for logs.

# Configuration

As always the configuration is in `defaults/main.yml` and mostly informs the `templates/kibana.yml.j2` template, but currently does not change the default behaviour much.

Most important setting is probably:

```yaml
kibana_domain: 'kibana.status.im'
```
