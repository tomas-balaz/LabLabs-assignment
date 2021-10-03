# TASK:
# Treba implementovat vramci zadania
#
# Aplikacia je by default dostupna na porte 8080

# Inspirovane podla https://docs.docker.com/language/golang/build-images/

FROM golang:1.16-alpine as builder

WORKDIR /build

COPY main.go ./
COPY go.mod ./

RUN go build -o ./go-app


FROM alpine:latest

WORKDIR /app
COPY --from=builder /build/go-app .

EXPOSE 8080

CMD [ "./go-app" ]
