FROM golang:1.16-alpine

WORKDIR /usr/src/app

COPY . .

RUN CGO_ENABLED=0 go build

EXPOSE 8080

CMD ["./server"]
