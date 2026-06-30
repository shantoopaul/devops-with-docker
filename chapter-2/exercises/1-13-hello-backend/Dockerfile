FROM golang:1.16-alpine

WORKDIR /usr/src/app

COPY . .

EXPOSE 8080

ENV PORT=8080 \
    REQUEST_ORIGIN="http://localhost:5001" \
    REDIS_HOST=redis-server


RUN apk update && apk add gcc musl-dev \ 
    && go build && go test ./...

CMD [ "./server" ]