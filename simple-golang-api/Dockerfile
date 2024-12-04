FROM golang:1.22-alpine3.20 AS builder

WORKDIR /build

COPY . .

# Сборка бинарного файла main
RUN go build -o main main.go

FROM alpine:3.20

COPY --from=builder /build/main /main

EXPOSE 8000

CMD ["./main"]
