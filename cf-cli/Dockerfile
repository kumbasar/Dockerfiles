FROM debian

WORKDIR /app

RUN apt-get -qq update && apt-get -qq -y install curl

RUN curl -L "https://cli.run.pivotal.io/stable?release=linux64-binary&source=github" | tar -zxf - -C /usr/bin

RUN cf -v
