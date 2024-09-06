![Elastic Image](elastic.svg)

### Elastic Search stack
this stack would use all Elastic Agents such as MetricBeats, FileBeats, HeartBeats. Each Agents are work their roles respectively, more information and documentation about BeatsFamily at [Here](https://www.elastic.co/beats).


### HOW TO USE
just run `sudo docker compose up -d` and all stack would run. Make sure to change `.env.sample` to `.env` and write your own password for kibana and elasticsearch.

### Configuration

| File  | Description  |
|---|---|
| /filebeat/filebeat.yml  | FileBeat configuration  |
| /mylog | log folder stored from host to docker, see `docker-compose.yaml/filebeat/volume` |
| /logstash/config/logstash.yml | logstash configuration listen from filebeat input to logstash |
| /logstash/config/pipelines.yml | create pipeline from output logstash from filebeat |
| /logstash/pipeline/logstash.conf | pipeline configuration |
| /metricbeat/metricbeat.yml | Metricbeat configuration (WIP) |