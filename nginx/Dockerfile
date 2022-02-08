FROM nginx:latest

RUN rm -f /var/log/nginx/access.log && rm -f /var/log/nginx/error.log

RUN curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.16.3-amd64.deb && \
  dpkg -i filebeat-7.16.3-amd64.deb

COPY filebeat.yml /etc/filebeat/filebeat.yml
RUN chmod go-w /etc/filebeat/filebeat.yml

RUN curl -L -O https://artifacts.elastic.co/downloads/beats/packetbeat/packetbeat-7.17.0-amd64.deb && \
  dpkg -i packetbeat-7.17.0-amd64.deb

COPY packetbeat.yml /etc/packetbeat/packetbeat.yml
RUN chmod go-w /etc/packetbeat/packetbeat.yml

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT [ "/entrypoint.sh" ]