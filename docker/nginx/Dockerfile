#
# TASK: Fix Dockerfile if anything is missing.
FROM nginx:alpine

# added
WORKDIR /app
ENV APP="sample-app"

COPY index.html /usr/share/nginx/html
COPY default.conf /etc/nginx/conf.d

COPY start.sh ./start.sh
RUN ["chmod", "+x", "./start.sh"]

EXPOSE 80

CMD ["./start.sh"]
