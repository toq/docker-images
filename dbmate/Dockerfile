FROM alpine:3.23
# https://stackoverflow.com/a/77726353
ARG TARGETARCH
RUN apk add --no-cache bash curl postgresql-client && \
  curl -L -o /usr/bin/dbmate 'https://github.com/amacneil/dbmate/releases/download/v2.31.0/dbmate-linux-${TARGETARCH}' && \
  chmod +x /usr/bin/dbmate

ENTRYPOINT ["dbmate"]
