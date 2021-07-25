# TASK:
# Treba implementovat vraci zadania
#
# Aplikacia je by default dostupna na porte 8080

# Inspirovane podla https://docs.docker.com/language/golang/build-images/

FROM golang:1.16-alpine

WORKDIR /app

COPY main.go ./
COPY go.mod ./

RUN go build -o ./go-app

EXPOSE 8080

CMD [ "./go-app" ]
