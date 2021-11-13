FROM node:15-alpine

RUN apk update && apk upgrade && apk add bash

ENV NODE_ENV=development

WORKDIR /usr/src/app

COPY package*.json /usr/src/app/

RUN npm install --progress=false --cache=false

COPY . /usr/src/app

ENV NUXT_HOST 0.0.0.0
ENV NUXT_PORT 3000
