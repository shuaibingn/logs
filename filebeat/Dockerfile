FROM docker.elastic.co/beats/filebeat:7.5.1

COPY ./config/filebeat.yml /usr/share/filebeat/filebeat.yml

WORKDIR /usr/share/filebeat/

CMD ["./filebeat", "-e", "-c", "./filebeat.yml", "-d", "publish"]
#CMD ["tail", "-f", "/dev/null"]