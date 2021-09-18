.PHONY: docker clean

docker: Dockerfile default.conf
# TASK: Build NGINX Docker image
	docker build -t tomasbalaz/sample-nginx:0.1 .

docker-run: docker
	docker run -d -p 8001:80 --name nginxProxy --env APP=http://$(docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' goBE):8080 tomasbalaz/sample-nginx:0.1

clean:
	docker rmi -f repo/sample-nginx:0.1 | true
