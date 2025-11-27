FROM node:18.19.0-alpine
LABEL maintainer "Peter Zhang <zhangchunsheng423@gmail.com>"
WORKDIR /app

# https://registry.npmmirror.com/
RUN npm install --global "pnpm" --registry=https://registry.npmmirror.com

COPY . .
RUN pnpm config set registry https://registry.npmmirror.com && pnpm install

ENV PLATFORM=PROD \
  IN_DOCKER=true

EXPOSE 3000
CMD node /app/app.js
