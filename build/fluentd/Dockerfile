FROM fluent/fluentd:latest
USER root
WORKDIR /home/fluent
ENV PATH /home/fluent/.gem/ruby/2.2.0/bin:$PATH
RUN apk --no-cache --update add geoip-dev build-base ruby-dev grep
RUN fluent-gem install fluent-plugin-record-reformer
RUN fluent-gem install fluent-plugin-rewrite
RUN fluent-gem install fluent-plugin-parser
RUN fluent-gem install fluent-plugin-elasticsearch
RUN fluent-gem install fluent-plugin-split
RUN fluent-gem install fluent-plugin-record-reformer
RUN fluent-gem install fluent-plugin-rewrite
RUN fluent-gem install fluent-plugin-parser
RUN fluent-gem install fluent-plugin-elasticsearch
RUN fluent-gem install fluent-plugin-split
RUN fluent-gem install fluent-plugin-rewrite-tag-filter
RUN fluent-gem install fluent-plugin-parser
RUN fluent-gem install fluent-plugin-suppress
RUN fluent-gem install fluent-plugin-mail
RUN fluent-gem install fluent-plugin-netflow
RUN fluent-gem install fluent-plugin-geoip
RUN fluent-gem install fluent-plugin-grep
RUN fluent-gem install fluent-plugin-record-modifier
RUN fluent-gem install fluent-plugin-elasticsearch-timestamp-check
EXPOSE 24284
CMD fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins $FLUENTD_OPT
