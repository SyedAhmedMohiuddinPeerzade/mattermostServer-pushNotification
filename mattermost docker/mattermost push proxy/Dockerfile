FROM frolvlad/alpine-glibc:alpine-3.6
MAINTAINER syed <ahmed.meraj89@gmail.com>

RUN apk add --no-cache ca-certificates curl \
	&& curl -sSL https://github.com/mattermost/mattermost-push-proxy/releases/download/v3.10/mattermost-push-proxy-3.10.0.tar.gz | tar -xz \
	&& mv /mattermost-push-proxy/bin/mattermost-push-proxy /push-proxy \
	&& chmod +x /push-proxy \
	&& rm -rf /mattermost-push-proxy \
	&& apk del curl \
       && mkdir /config
COPY scripts /scripts

EXPOSE 8066
ENTRYPOINT ["/scripts/entry"]

