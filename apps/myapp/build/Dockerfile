FROM docker.io/golang:1.20

WORKDIR /usr/src/app

COPY go.mod go.sum .
RUN go mod download

COPY . .
RUN go build ./apps/myapp

RUN go run ./apps/myapp
