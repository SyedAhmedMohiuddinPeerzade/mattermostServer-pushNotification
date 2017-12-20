FROM ubuntu:16.04

ENV PATH="/mattermost/bin:${PATH}"


RUN apt-get update \
    && apt-get -y install \
      curl \
      jq \
      netcat \
      net-tools \
      iproute \
      dnsutils

# Prepare Mattermost
RUN mkdir -p /mattermost/data \
    && curl https://releases.mattermost.com/4.5.0/mattermost-4.5.0-linux-amd64.tar.gz | tar -xvz \
    && rm -rf /mattermost/config/config.json

COPY config.template.json / 
COPY scripts /scripts
EXPOSE 8065
EXPOSE 8067
EXPOSE 8074
EXPOSE 8075
WORKDIR /mattermost/bin
ENTRYPOINT ["/scripts/entry.sh"]
