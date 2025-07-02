FROM golang:1.16-alpine

WORKDIR /usr/src/app

COPY go.mod go.sum ./

RUN go mod download

COPY . . 

RUN go build -o server

EXPOSE 8080

ENV PORT=8080
ENV REQUEST_ORIGIN=http://localhost:5000

CMD ["./server"]
