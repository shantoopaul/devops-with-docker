FROM node:16-alpine

EXPOSE 5001

WORKDIR /usr/src/app

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN apk update \
    && npm install \
    && npm install -g serve \
    && npm run build

CMD [ "serve", "-s", "-l", "5001", "build" ]