FROM golang:1.16-alpine

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

ENV PORT=8080
ENV REQUEST_ORIGIN="http://localhost:5001"

RUN apk update && apk add gcc musl-dev \ 
    && go build && go test ./...

CMD [ "./server" ]