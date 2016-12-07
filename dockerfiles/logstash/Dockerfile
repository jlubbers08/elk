FROM debian:jessie
RUN apt-get update && \
    apt-get install -y wget
RUN wget https://artifacts.elastic.co/downloads/logstash/logstash-5.0.2.deb -O /tmp/logstash.deb
    dpkg -i /tmp/logstash.deb ; \
    dpkg -i /tmp/logstash-contrib.deb ; \
    apt-get -f -y install && \
    rm -rf /tmp/logstash.deb /tmp/logstash-contrib.deb
COPY logstash.sample.conf /etc/logstash.sample.conf
ENTRYPOINT ["/opt/logstash/bin/logstash"]
CMD []
