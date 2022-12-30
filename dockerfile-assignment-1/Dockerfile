# use this empty Dockerfile to build your assignment
FROM node:6-alpine
# NOTE: The instructions are now in the README.md file in this directory.
EXPOSE 3000

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean --force

COPY . .

CMD [ "/sbin/tini", "--", "node", "./bin/www" ]
