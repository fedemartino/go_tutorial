FROM golang:1.24.4

WORKDIR /app

COPY go.mod ./

RUN go mod download

COPY *.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /go-http-test

EXPOSE 80

CMD ["/go-http-test"]