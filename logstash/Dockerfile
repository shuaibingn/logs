FROM logstash:7.5.1

COPY ./pipeline/logstash.conf /usr/share/logstash/pipeline/
COPY ./config/* /usr/share/logstash/config/

WORKDIR /usr/share/logstash/
RUN ./bin/logstash-plugin install logstash-output-stomp

CMD ["./bin/logstash", "-f", "./pipeline/logstash.conf"]
#CMD ["tail", "-f", "/dev/null"]