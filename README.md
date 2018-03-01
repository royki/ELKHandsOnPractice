
#####_ELK Stack_

- `Elasticsearch` – It stores incoming logs from Logstash and provides an ability to search the logs/data in a real time
- `Logstash` – Logstash is a data processing pipeline for managing events and logs; processes (Collect, enrich and send it to Elasticsearch)
- `Kibana` – Provides visualization of logs.
- `Beats` – Installed on client machines, send logs to `Logstash` through beats protocol.
    - `Packetbeat` – Analyze network packet data.
    - `Filebeat` – Real-time insight into log data.
    - `Topbeat` – Get insights from infrastructure data.
    - `Metricbeat` – Ship metrics to Elasticsearch.



