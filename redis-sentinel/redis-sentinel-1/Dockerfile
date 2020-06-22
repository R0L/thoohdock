FROM redis:latest

LABEL maintainer="Mahmoud Zalt <mahmoud@zalt.me>"

## For security settings uncomment, make the dir, copy conf, and also start with the conf, to use it
RUN mkdir -p /usr/local/etc/redis
COPY sentinel.conf /usr/local/etc/redis/sentinel.conf

RUN mkdir -p /var/log/redis /var/lib/redis
RUN chmod 777 -R /var/log/redis /var/lib/redis

VOLUME /data

EXPOSE 6379

CMD ["redis-sentinel", "/usr/local/etc/redis/sentinel.conf"]
#CMD ["redis-server"]
