FROM fluent/fluentd:latest
USER fluent
WORKDIR /home/fluent
ENV PATH /home/fluent/.gem/ruby/2.2.0/bin:$PATH
RUN fluent-gem install fluent-plugin-route
RUN fluent-gem install fluent-plugin-conditional_filter
RUN fluent-gem install fluent-plugin-rewrite-tag-filter
RUN fluent-gem install fluent-plugin-unique-counter
RUN fluent-gem install fluent-plugin-grep
RUN fluent-gem install fluent-plugin-rewrite-tag-filter
RUN fluent-gem install fluent-plugin-parser
RUN fluent-gem install fluent-plugin-hostname
RUN fluent-gem install fluent-plugin-grok-parser
RUN fluent-gem install fluent-plugin-suppress
RUN fluent-gem install fluent-plugin-record-reformer
RUN fluent-gem install fluent-plugin-mail
RUN fluent-gem install fluent-plugin-elasticsearch
RUN fluent-gem install fluent-plugin-multi-format-parser
RUN fluent-gem install fluent-plugin-numeric-counter
RUN fluent-gem install fluent-plugin-split
RUN fluent-gem install fluent-plugin-rewrite
RUN fluent-gem install fluent-plugin-resolv
EXPOSE 24284
CMD fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins $FLUENTD_OPT
