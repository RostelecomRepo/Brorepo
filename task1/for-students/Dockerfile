FROM golang:1.16-alpine as builder
WORKDIR /build
COPY . .
RUN go build -o /app app.go
FROM alpine:3
COPY --from=builder app /bin/app
ENTRYPOINT ["/bin/app"]
