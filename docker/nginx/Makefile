.PHONY: docker clean

docker: Dockerfile default.conf
# TASK: Build NGINX Docker image
	docker build -t tomasbalaz/sample-nginx:0.1 .

clean:
	docker rmi -f repo/sample-nginx:0.1 | true
