FROM ubuntu:16.04
COPY ./bin/deployment-v1.sh /tmp/build.sh

RUN chmod +x /tmp/build.sh

RUN LC_ALL=C DEBIAN_FRONTEND=noninteractive /tmp/build.sh \
  && rm -rf /var/lib/apt/lists/*