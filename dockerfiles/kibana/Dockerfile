FROM nginx:1
RUN apt-get update && apt-get install -y wget ca-certificates
RUN wget https://artifacts.elastic.co/downloads/kibana/kibana-5.0.2-amd64.deb -O /tmp/kibana.tar.gz && \
    cd /tmp && tar zxf kibana.tar.gz && mv kibana-*/* /usr/share/nginx/html/
EXPOSE 80
