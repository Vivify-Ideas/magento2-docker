FROM elasticsearch:5.6

WORKDIR /usr/share/elasticsearch

RUN apt-get update && \
    bin/elasticsearch-plugin install analysis-phonetic \
    && bin/elasticsearch-plugin install analysis-icu;