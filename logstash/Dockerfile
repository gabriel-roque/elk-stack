ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:8.0.1

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json

RUN sh -c 'bin/logstash-plugin install logstash-input-beats'
RUN sh -c 'bin/logstash-plugin install logstash-filter-json'
RUN sh -c 'bin/logstash-plugin install logstash-filter-mutate'
