FROM ubuntu:26.04

EXPOSE 5001

WORKDIR /usr/src/app

COPY . .

RUN apt-get update \
    && apt-get install -y curl \
    && curl -sL https://deb.nodesource.com/setup_16.x | bash \
    && apt install -y nodejs \
    && node -v \
    && npm -v \
    && npm install \
    && npm install -g serve \
    && npm run build

CMD [ "serve", "-s", "-l", "5001", "build" ]