FROM node:11.1.0-alpine

WORKDIR /app

ADD ./client/package.json ./client/yarn.lock /tmp/
RUN cd /tmp && yarn
RUN cd /app && ln -s /tmp/node_modules

COPY ./client ./

EXPOSE 3000
CMD ["yarn", "start"]
