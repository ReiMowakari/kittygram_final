FROM node:18
RUN echo "${DOCKER_USERNAME}" > /tmp/docker_username && chmod 0400 /tmp/docker_username
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm ci

COPY . .
RUN npm run build
RUN npm install --global http-server

CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]
