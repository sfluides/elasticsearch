FROM elasticsearch:2.4.0

WORKDIR /usr/share/elasticsearch

COPY config ./config

# install couchbase plugin
RUN echo y | bin/plugin install https://github.com/couchbaselabs/elasticsearch-transport-couchbase/releases/download/2.2.4.0-update1/elasticsearch-transport-couchbase-2.2.4.0-update1.zip

# install head plugin
RUN bin/plugin install mobz/elasticsearch-head 

# expose 9091 port for couchbase plugin
EXPOSE 9091