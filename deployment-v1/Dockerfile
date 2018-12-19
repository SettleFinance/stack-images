FROM ubuntu:16.04
COPY ./bin/deployment-v1.sh /tmp/build.sh

RUN chmod +x /tmp/build.sh

RUN LC_ALL=C DEBIAN_FRONTEND=noninteractive /tmp/build.sh \
  && rm -rf /var/lib/apt/lists/*

ARG DEBIAN_FRONTEND=noninteractive
RUN curl -sL https://deb.nodesource.com/setup_11.x | bash -
RUN apt-get update && apt-get -qq install -y nodejs && apt-get -qq install -y nginx

RUN npm install -g @angular/cli
#RUN npm install --save-dev @angular-devkit/build-angular
RUN npm install -g heroku

