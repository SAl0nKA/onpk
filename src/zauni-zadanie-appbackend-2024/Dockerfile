# Multi-stage build docker file

# app build stage
FROM golang:alpine as builder
RUN mkdir /build
COPY . /build
WORKDIR /build

RUN CGO_ENABLED=0 GOOS=linux go build -a -o main .

# image build image - use scratch to get smallest possible size of an image
FROM scratch

COPY --from=builder /build/main /app/
WORKDIR /app
CMD ["./main"]

