FROM node:latest
ARG frontpath
WORKDIR /app
COPY $frontpath .
RUN yarn global add @quasar/cli

RUN yarn install

RUN npm install -g serve

CMD yarn build:prod ; serve -l 8080 dist

