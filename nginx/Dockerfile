FROM nginx:1.22.1
RUN echo "${DOCKER_USERNAME}" > /tmp/docker_username && chmod 0400 /tmp/docker_username
COPY nginx.conf /etc/nginx/templates/default.conf.template
