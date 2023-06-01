FROM docker.io/golang:1.20

RUN apt update && apt install -y tree

WORKDIR /usr/src/app

COPY go.mod go.sum .
RUN go mod download

COPY . .
RUN tree
RUN go build ./apps/myapp

RUN go run ./apps/myapp
