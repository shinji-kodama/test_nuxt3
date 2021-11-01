FROM node:17.0-alpine3.12
ENV HOST 0.0.0.0
# コマンド実行
RUN apk update && \
    apk add git && \
    npx nuxi init nuxt3-app \