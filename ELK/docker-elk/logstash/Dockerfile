ARG ELASTIC_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELASTIC_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
# https://www.elastic.co/guide/en/logstash/current/plugins-inputs-rabbitmq.html
RUN logstash-plugin install logstash-integration-rabbitmq
