FROM node:alpine AS build

WORKDIR /app
RUN apk add --no-cache --virtual .gyp python make g++

COPY ./app/ .

RUN yarn --frozen-lockfile --non-interactive \
    && yarn build


FROM httpd:2.4
COPY --from=build --chown=www-data:www-data /app/public /usr/local/apache2/htdocs/
