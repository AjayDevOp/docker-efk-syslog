# Docker-elk-syslog

1. git pull https://github.com/kkniffin/docker-elk-syslog
2. chmod -R 777 ./elasticsearch/data
3. curl -XPUT http://localhost:9200/_template/logstash_per_index -d @elasticsearch/config/templates/logstash-template.json
4. curl -XPUT http://localhost:9200/_template/netflow_per_index -d @elasticsearch/config/templates/netflow-template.json
