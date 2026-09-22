ARG debian_version=13-slim

FROM debian:${debian_version}
RUN DEBIAN_FRONTEND=noninteractive \
  apt-get update && \
  apt-get install -y --no-install-recommends ca-certificates gnupg curl && \
  . /etc/os-release && \
  curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc | gpg -o /usr/share/keyrings/postgresql.gpg --dearmor && \
  echo "deb [ signed-by=/usr/share/keyrings/postgresql.gpg ] https://apt.postgresql.org/pub/repos/apt ${VERSION_CODENAME}-pgdg main" | tee /etc/apt/sources.list.d/pgdg.list && \
  apt-get update && \
  apt-get install -y zstd screen wget htop tree vim make postgresql-client-18 && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
CMD ["sleep", "inf"]
