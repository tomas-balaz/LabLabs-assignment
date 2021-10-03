.PHONY: docker docker-run clean

backend: main.go
	CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o backend .

docker: Dockerfile backend
# TASK: Build docker image here
	docker build -t tomasbalaz/sample-backend:0.1 .

docker-run: docker
	docker run -d -p 9990:8080 --name goBE tomasbalaz/sample-backend:0.2

clean:
	rm -rf backend
	docker rmi -f tomasbalaz/sample-backend:0.1 | true
